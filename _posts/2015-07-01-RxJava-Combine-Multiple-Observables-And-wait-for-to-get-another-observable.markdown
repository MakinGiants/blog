---
title: RxJava/Retrofit combine multiple observables and wait for to get another observable.
layout: post
date: 2015-07-01 07:10:00 GCM-5
updated: 2015-07-01 07:10:00 GCM-5
comments: false
categories: Android RXJava Retrofit
---

Sometimes we need to get some data before do something else, each one can be from
different sources, like 2 different web services.

*Using `Retrofit 1.9` and `retrolambda`*

* `NewOrder` is the object that we need to create from 2 data sources, 
both getted from an `Observable<Address>`.

{% highlight java %}
class NewOrder {
	
	...

	public NewOrder(Address dropAddress, Address pickAddress){
		...
	}

}
{% endhighlight %}

The Retrofit service that consumes the object and creates the final Observable:

{% highlight java %}
@POST("url")
Observable<Order> create(@Body NewOrder id);
{% endhighlight %}

* We will have 2 Observables to wait for result: `pickObservable` and `dropObservable`. (can be more! just add each Observable to combineLatest`)

* `Address.get(...)` is a function that will return an observable with the address for that LatLng.
 
* Use `Observable.combineLatest` to combine both `pickObservable` and `dropObservable` and wait
for it´s results and will end in a new `Observable<NewOrder>`.

* Use flatMap to apply 

{% highlight java %}
public static Observable<Order> create(final OrderData orderData) {
   	// Prerequisites
    Observable<Address> pickObservable = Address.get(new LatLng(1.2. -1,2));
    Observable<Address> dropObservable = Address.get(new LatLng(1.2. -1,2);

    // Create a new Observer that will end until both observables get data.
    Observable<NewOrder> newOrderObservable = 
    	Observable.combineLatest(pickObservable, dropObservable
            (pickAddress, dropAddress,) ->
                    new NewOrder(pickAddress, dropAddress)
    );

    // create new observable from last observable.
    return newOrderObservable.flatMap(order -> create(order));
}

private static Observable<Order> create(OrderService.NewOrder newOrder) {
    return SERVICE.createOrder(newOrder);
}

{% endhighlight %}

Thanks to [lukaciko](http://stackoverflow.com/users/971273/lukaciko).
Check this [question on stackoverflow](http://stackoverflow.com/questions/31170677/rxjava-android-observable-result-needed-to-create-another-observable).