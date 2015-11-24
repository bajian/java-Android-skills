# java-Android-skills
Android程序中开发经验-技巧总结

***
####
```

```

***
####将子线程中的结果回调到主线程中：
```
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
