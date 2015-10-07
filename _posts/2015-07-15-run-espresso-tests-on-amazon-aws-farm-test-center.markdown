---
layout: post
title: "Run Espresso tests on Amazon AWS Farm test center"
date: 2015-07-15
updated: 2015-10-07
categories: Android
---

# For JUnit 3

For [AWS Device farm](aws.amazon.com/device-farm/) you need to upload both apk, your app apk and your tests apk.

1. Run assemble task for AndroidTest.
{% highlight bash %}
# ./gradlew assembleDebugAndroidTest
{% endhighlight %}
**NOTE**: Debug is the buildType.

2. Check generated apks:
* app.apk: `app/build/output/apk/app-debug.apk`.
* test.apk: `app/build/output/apk/app-debug-androidTest-unaligned.apk`.

# For JUnit 4 and Testing Support Library support

Oficial JUnit tags are not supported so you need to format names with:
1. Your test class should end with "Tests".
2. Your tests method should start wiht "test".

Example:

{% highlight java %}
@RunWith(AndroidJUnit4.class)
@LargeTest
public class LoginActivityTests {

	@Rule
	public ActivityTestRule<LoginActivity> mActivityRule = new ActivityTestRule(LoginActivity.class);

	@Before
	public void setup() {
	}

	@Test
	public void testShowsRightDataOnCreate() {
		org.junit.Assert.assertEquals("asd", "asd");
	}
}
{% endhighlight %}


# Links
- [AWS forum](https://forums.aws.amazon.com/thread.jspa?messageID=678960&#678960)

Tested and working.