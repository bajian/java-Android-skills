# java-Android-skills
Android程序中开发经验-技巧总结

***
####
```

```
***
####做APP需要哪些工具？年度最新移动应用工具盘点（内附福利）
```
http://mp.weixin.qq.com/s?__biz=MzA4NDE2MzE4OA==&mid=403886612&idx=2&sn=68b378050c9c17cb2543ce7a41f92d95&scene=23&srcid=11187TxPRngqJ0B8pDpFu1dO#rd
```


***
####activity 四种启动方式。老是看了忘
```
http://blog.csdn.net/zapzqc/article/details/8493481

```

***
####Activity以singleTask模式启动，intent传值的解决办法
```
http://www.mamicode.com/info-detail-872224.html


```

***
####Android开发 旋转屏幕导致Activity重建解决方法
```
http://www.jb51.net/article/31833.htm
```


***
####String s=new String("abc")创建了几个对象?
```
http://blog.csdn.net/caiwenfeng_for_23/article/details/46841833
```

***
####gradle教程
```
http://ask.android-studio.org/?/explore/category-gradle
```


***
####ListView的item点击无响应的解决方法
```

```
http://blog.csdn.net/caiwenfeng_for_23/article/details/37760197
如果listitem里面包括button或者checkbox等控件，默认情况下listitem会失去焦点，导致无法响应item的事件，最常用的解决办法
是在listitem的item布局文件中设置descendantFocusability属性。

beforeDescendants：viewgroup会优先其子类控件而获取到焦点
        afterDescendants：viewgroup只有当其子类控件不需要获取焦点时才获取焦点
        blocksDescendants：viewgroup会覆盖子类控件而直接获得焦点
***
####将子线程中的结果回调到主线程中：
```
https://github.com/bajian/MainThreadCallbackDemo

	mDelivery = new Handler(Looper.getMainLooper());
	
    public void sendFailResultCallback(final Request request, final Exception e, final ResultCallback callback)
    {
        if (callback == null) return;

        mDelivery.post(new Runnable()
        {
            @Override
            public void run()
            {
                callback.onError(request, e);
                callback.onAfter();
            }
        });
    }

```
