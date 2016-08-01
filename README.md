SwipeBack
====================================

Features
--------

- 无需设置theme背景透明等属性,与 `<item name="android:windowIsTranslucent">true</item>` 没有任何关系 
- 不影响activity的生命周期
- 只需继承BaseActivity，即可实现滑动返回      
- 对外只暴露了一个api  `isSupportSwipeBack`  ,简单实用   

Usage
--------


#### 包括以下6中状态  

```java  

    private static final int MSG_ACTION_DOWN = 1; //点击事件  
    private static final int MSG_ACTION_MOVE = 2; //滑动事件
    private static final int MSG_ACTION_UP = 3;  //点击结束
    private static final int MSG_SLIDE_CANCEL = 4; //开始滑动，不返回前一个页面
    private static final int MSG_SLIDE_CANCELED = 5;  //结束滑动，不返回前一个页面
    private static final int MSG_SLIDE_PROCEED = 6; //开始滑动，返回前一个页面
    private static final int MSG_SLIDE_FINISHED = 7;//结束滑动，返回前一个页面
```

#### 自定义方法 
默认activity是支持滑动返回的，不需要返回的则需要复写Baseactivity的以下方法  
```java

      /**
     * 是否支持滑动返回
     *
     * @return
     */  
    protected boolean supportSlideBack() {
        return true;
    }  
```


ScreenShot
---------

![image](./screenshot/swipeback.gif)
