---
layout: post
title: "Mock Retrofit service using MockRestAdapter and Espresso 2.0 (No Mockito)"
date: "2015-07-02"

categories: Android Espresso Retrofit
---

*Note:* **DON'T DO THIS!** check the end of the post to know why.

I will not use mockito because it give me so much errors, when we will use

* `Android Support Test`: runner, rules and espresso.
* `jUnit4`: as base tests.
* `assertj-android`: because is so cool.
* `retrofit-mock`: to mock our services.

You need to add as dependency:

{% highlight groovy %}
dependencies {
    androidTestCompile 'com.android.support.test:runner:0.3'
    androidTestCompile 'com.android.support.test:rules:0.3'
    androidTestCompile 'com.android.support:support-annotations:22.2.0'
    androidTestCompile 'com.android.support.test.espresso:espresso-core:2.2'
    androidTestCompile 'junit:junit:4.12'
    androidTestCompile 'com.squareup.retrofit:retrofit-mock:1.9.0'
    androidTestCompile('com.squareup.assertj:assertj-android:1.0.0') {
        exclude group: 'com.android.support', module: 'support-annotations'
    }
}
{% endhighlight %}

The project will use Order.get("id") to get the observable, inside of it we will call the retrofit reacted
service to get the data and return it (process it before if we need to, por ex save into shared preferences).
The idea is to override that service instance that Order have with the mocked one created using `MockRestAdapter`
from retrofit guys.

We will need:

1. A normal retrofit service interface (`OrderService`).

{% highlight java %}
@VisibleForTesting
public interface OrderService {

    @GET("/api/{id}")
    Observable<Order> get(@Path("id") String id);
}
{% endhighlight %}

2. A mock service that returns what we want (`MockedOrderService`).

{% highlight java %}
public class MockOrderService implements OrderService {

    private Order mOrder;

    public static void mock(Order order){
        mOrder = order;

        // Setup MockRestAdapter without delays or posible errors
        MockRestAdapter mockRestAdapter = MockRestAdapter.from(ApiManager.REST_ADAPTER);
        mockRestAdapter.setDelay(0);
        mockRestAdapter.setErrorPercentage(0);
        mockRestAdapter.setVariancePercentage(0);

        // Create the mocked service and replace it in
        MockOrderService mockOrderService = new MockOrderService();
        mockOrderService.mOrder = order;

        // Replace the service instance with the mocked one
        // Then every time that the projec call Order.get will return what we
        // had in our MockOrderService.get() code
        Order.SERVICE = mockRestAdapter.create(OrderService.class, mockOrderService);
    }

    // OrderService override
    @Override
    public Observable<Order> get(@Path("id") String id) {
        return Observable.just(mOrder);
    }

}
{% endhighlight %}

3. Everytime before the activity is created on the tests we should replace the service instance on the app
with the mocked one.
*Note* it uses `@VisibleForTesting` from support-annotations notation to show that it should be private but is public to allow
us to change it´s value on tests.

{% highlight java %}
public class Order  {

    @VisibleForTesting
    public static OrderService SERVICE = ApiManager.REST_ADAPTER.create(OrderService.class);

    public Observable<Order> get(String id){
        return SERVICE.get(id);
    }
}

public class ApiManager {

    public static RestAdapter REST_ADAPTER;

    static {
        REST_ADAPTER = new RestAdapter.Builder()
                .setEndpoint(host)
                .build();
    }
}
{% endhighlight %}

And then our tests will look like:

{% highlight java %}
@RunWith(AndroidJUnit4.class)
@LargeTest
public class SomeActivityTests {

    @Rule
    public ActivityTestRule<SomeActivity> mActivityRule = new ActivityTestRule<>(SomeActivity.class);

    @Test
    public void successCloseView() {
        MockResponse<Response> mockResponse = new MockResponse<>(response(200, "{ \"status\": 200 }"));
        MockOrderService.mock(new Order("Name"));

        //... Do the espresso things...
    }

}
{% endhighlight %}

*Note:* Be careful if your activity use the services `onResume` or `onStart` because then we will need to start the activity
JUST after we mocked the services (The last example mock it after becuase `@Rule` starts activity automatically).
Then we need to put `true, false` in the ActivityTestRule constructor to avoid that and start manually.

{% highlight java %}
@RunWith(AndroidJUnit4.class)
@LargeTest
public class SomeActivityTests {

    @Rule
    public ActivityTestRule<SomeActivity> mActivityRule = new ActivityTestRule<>(SomeActivity.class, true, false);

    @Test
    public void successCloseView() {
        MockResponse<Response> mockResponse = new MockResponse<>(response(200, "{ \"status\": 200 }"));
        MockOrderService.mock(new Order("Name"));

        // with launchActivity we start the activity after we mocked the service.
        mActivityRule.launchActivity(new Intent());
        //... Do the espresso things...
    }

}
{% endhighlight %}

Thansk to Retrofit guys for everything!.

# EDIT

If you end trying to do something like this maybe you have a ~~terrible~~ not testeable code structure, so please don't do it. It will be hard to change and really really hard to understand.

At the end I removed every espresso test and start using MVP in all the project,
then I can run my tests just on JVM (Yeah, no more android emulator).

Check Mockito or Powermock for mocking the api responses, and if you try and you can't again is posible that you have a terrible code structure.
