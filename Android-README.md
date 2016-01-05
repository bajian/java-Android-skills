# java-Android-skills
Android程序中开发经验-技巧总结--及一些干货

***
####
```

```

***
####Android InputMethodManager
```
Android InputMethodManager输入法简介
http://www.cnblogs.com/weixing/p/3300908.html

```
***
####Android中Handler引起的内存泄露
```
http://droidyue.com/blog/2014/12/28/in-android-handler-classes-should-be-static-or-leaks-might-occur/

细话Java："失效"的private修饰符
http://droidyue.com/blog/2014/10/02/the-private-modifier-in-java/

java中，什么是对象的可达与不可达？
http://zhidao.baidu.com/link?url=ljcxE68MhHWBU3IeZGosmFFH5PBp17A7uzRSBKFD_nMoS7Z5yyKbrIbqvx5WdLB0Ra6d3LsboUJtK1V4z5qsQq

```

***
####非UI线程可以去刷新UI吗（rogressbar的setProgress的特例）
```
http://blog.csdn.net/androidzhaoxiaogang/article/details/8136222

```

***
####[Android Memory] android 警告：Exported activity does not require permission
```
http://www.cnblogs.com/0616--ataozhijia/p/3738569.html

```


***
####java 注解
```
注解的继承关系
http://elf8848.iteye.com/blog/1621392
```

***
####Android studio NDK开发
```

Android studio NDK开发
http://www.th7.cn/Program/Android/201509/550864.shtml
一系列文章
http://blog.csdn.net/yanbober/article/details/45310365
```

***
####android 持久化保存cookie
```
DEMO:
https://github.com/bajian/LeagueSharpLoginDemo
注解的继承关系
http://blog.csdn.net/jwzhangjie/article/details/29861111

Android OkHttp的Cookie自动化管理
http://www.2cto.com/kf/201507/419264.html
```

***
####做APP需要哪些工具？年度最新移动应用工具盘点（内附福利）
```
http://mp.weixin.qq.com/s?__biz=MzA4NDE2MzE4OA==&mid=403886612&idx=2&sn=68b378050c9c17cb2543ce7a41f92d95&scene=23&srcid=11187TxPRngqJ0B8pDpFu1dO#rd

http://www.apicloud.com/modulestore很多实用模块

```

***
####java 合并两个byte数组  
```
    public static byte[] byteMerger(byte[] byte_1, byte[] byte_2){  
        byte[] byte_3 = new byte[byte_1.length+byte_2.length];  
        System.arraycopy(byte_1, 0, byte_3, 0, byte_1.length);  
        System.arraycopy(byte_2, 0, byte_3, byte_1.length, byte_2.length);  
        return byte_3;  
    }  

```
***
####java 反射与IoC DI 
```
class.forName()与ClassLoader：
http://blog.csdn.net/yanwushu/article/details/7574713

java中的反射，invoke方法
http://blog.sina.com.cn/s/blog_64e467d60100yqz9.html

利用Java的反射与代理机制实现IOC：
http://www.blogjava.net/amigoxie/archive/2007/10/12/152413.html

java的反射机制浅谈
http://blog.csdn.net/nieweilin/article/details/5908165

java动态代理（JDK和cglib）
http://www.cnblogs.com/jqyp/archive/2010/08/20/1805041.html

field.get(object) //取值
```

***
####安卓android APP切图规范和.9png制作教程
```
http://www.25xt.com/allcode/6370.html

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
注意事项：
http://blog.csdn.net/caiwenfeng_for_23/article/details/46918743


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
android listview里包含组件(checkbox)点击事件和Item的点击事件冲突
http://blog.csdn.net/caiwenfeng_for_23/article/details/46761687

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
