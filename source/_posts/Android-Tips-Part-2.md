title: "Android Tips Part 2"
date: 2015-03-23 14:33:12
tags:
---

> 原文作者：[Dan Lew](http://blog.danlew.net/about/)
> 原文地址：[Android Tips Round-Up, Part 2](http://blog.danlew.net/2014/04/14/android-tips-round-up-part-2/)

* [``DateUtils.formatDateTime()``][a]

	格式化日期/时间，输出为本地化格式。

* [``AlarmManager.setInexactRepeating``][b]

	注册一个非精密的重复类型定时器，系统会通过分组来节约电量。
	
* [``Formatter.formatFileSize()``][c]
	
	文件大小的本地化格式器。	

<!--more-->

* [``ActionBar.hide()``][d]``/``[``.show()``][e] 

	使用动画来``出现/隐藏ActionBar``，使得切换全屏时能够更平滑。

* [``Linkify.addLinks()``][f]

	通过它可以控制``TextView``显示内容的链接。

* [``StaticLayout``][g]

	在自定义View时，方便测试text。

* [``Activity.onBackPressed()``][h]

	方便处理返回键。虽然我经常不拦截返回键，但经常需要拦截返回键，从而保证正确的工作流。

* [``GestureDetector``][i]

	便捷的手势识别类。

* [``DrawFilter``][j]

	尽管没有调用view的draw相关方法，仍然可以通过它获取到Canvas对象。比如，自定义View时，可以设置``DrawFilter``来抗锯齿。
	
* [``ActivityManager.getMemoryClass()``][k]

	通过它，可以获取该设备可用内存的大小。根据该大小可以方便算出App缓存的大小。

* [``SystemClock.sleep()``][l]

	这个方法就是封装了Thread.sleep方法，但是不会抛出InterruptedException。能够方便的保证sleep一段时间。经常使用它来模拟网络延时。

* [``ViewStub``][m]

	一个轻量级的View，ViewStub是不可见的、不占用布局空间的视图，用于在运行时延迟加载布局资源. 当ViewStub可见，或者调用 inflate()函数时，才会加载布局资源.

* [``DisplayMetrics.density``][n]

	你可以通过该方法获取屏幕的密度。大部分情况下，最好让系统自动处理dimen的缩放。偶尔需要处理缩放时，非常有效，特别是在自定义View时。

* [``Pair.create()``][o]

	方便的工具类。


[a]: http://developer.android.com/reference/android/text/format/DateUtils.html#formatDateTime(android.content.Context,%20long,%20int)
[b]: http://developer.android.com/reference/android/app/AlarmManager.html#setInexactRepeating(int,long,long,android.app.PendingIntent)
[c]: http://developer.android.com/reference/android/text/format/Formatter.html#formatFileSize(android.content.Context,%20long)
[d]: http://developer.android.com/reference/android/app/ActionBar.html#hide()
[e]: http://developer.android.com/reference/android/app/ActionBar.html#show()
[f]: http://developer.android.com/reference/android/text/util/Linkify.html#addLinks(android.text.Spannable,%20int)
[g]: http://developer.android.com/reference/android/text/StaticLayout.html
[h]: http://developer.android.com/reference/android/app/Activity.html#onBackPressed()
[i]: http://developer.android.com/reference/android/view/GestureDetector.html
[j]: http://developer.android.com/reference/android/graphics/DrawFilter.html
[k]: http://developer.android.com/reference/android/app/ActivityManager.html#getMemoryClass()
[l]: http://developer.android.com/reference/android/os/SystemClock.html#sleep(long)
[m]: http://developer.android.com/reference/android/view/ViewStub.html
[n]: http://developer.android.com/reference/android/util/DisplayMetrics.html#density
[o]: http://developer.android.com/reference/android/util/Pair.html#create(A,%20B)