title: "Android Tips Part 1"
date: 2015-04-03 11:20:02
tags:
---

> 原文作者：[Dan Lew](http://blog.danlew.net/about/)
> 原文地址：[Android Tips Round-Up, Part 1](http://blog.danlew.net/2014/03/30/android-tips-round-up-part-1/)

* [``Activity.startActivities()``][a]

	当需要启动Activity栈中间的Activity时，非常有效。

* [``TextUtils.isEmpty()``][b]

	判断字符串是否为null或者“”，经常用到的工具类。

* [``Html.fromHtml()``][c]

	快速格式化HTML的一个方法。不是十分高效，所以我不是经常性使用，但是对于渲染从web server获取的HTML内容十分方便。

<!--more-->

* [``TextView.setError()``](http://developer.android.com/reference/android/widget/TextView.html#setError%28java.lang.CharSequence%29)

	校验输入时，方便使用的提示。

* [``Build.VERSION_CODES``](http://developer.android.com/reference/android/os/Build.VERSION_CODES.html)

	不仅可以在代码中避免硬编码，而且可以区分不同Android版本特性。

* [``Log.getStackTraceString()``][d]

	打印log时，有效的工具类。

* [``LayoutInflater.from()``](http://developer.android.com/reference/android/view/LayoutInflater.html#from%28android.content.Context%29)

	获取LayoutInflater的一种简单方式。

* [``ViewConfiguration.getScaledTouchSlop()``](http://developer.android.com/reference/android/view/ViewConfiguration.html#getScaledTouchSlop%28%29)

	通过ViewConfiguration.getScaledTouchSlop()获取到配置，可以确保App在Android系统中触摸事件体验的一致性。

* [``PhoneNumberUtils.convertKeypadLettersToDigits``](http://developer.android.com/reference/android/telephony/PhoneNumberUtils.html#convertKeypadLettersToDigits%28java.lang.String%29)

	处理电话号码的一种有效工具类。

* [``Context.getCacheDir()``](http://developer.android.com/reference/android/content/Context.html#getCacheDir%28%29)

	获取App的缓存目录。非常简单，但不是所有人都知道。

* [``ArgbEvaluator``](http://developer.android.com/reference/android/animation/ArgbEvaluator.html)

	转换颜色。[正如Chris Banes指出的](https://plus.google.com/+DanielLew/posts/SbieMPqa2by)，

* [``ContextThemeWrapper``](http://developer.android.com/reference/android/view/ContextThemeWrapper.html)

	更换主题十分高效。

* [``Space``](http://developer.android.com/reference/android/widget/Space.html)

	draw间隔经常使用到的一个轻量级View。

* [``ValueAnimator.reverse()``](http://developer.android.com/reference/android/animation/ValueAnimator.html#reverse%28%29)

	取消动画时，依然保持流畅。



[a]: http://developer.android.com/reference/android/app/Activity.html#startActivities(android.content.Intent[])
[b]: http://developer.android.com/reference/android/text/TextUtils.html#isEmpty(java.lang.CharSequence)
[c]: http://developer.android.com/reference/android/text/Html.html#fromHtml(java.lang.String)
[d]: http://developer.android.com/reference/android/util/Log.html#getStackTraceString(java.lang.Throwable)