# BackgroundFuzzy

适合对于用户信息隐私程度较高，涉及交易类移动端产品的隐私以及信息安全。

iOS平台，仿支付宝双击Home键进入后台后添加在Window层添加一层蒙版，保存用户安全隐私。

对于UIImage类进行方法扩展，提供类方法生成与屏幕统一尺寸的蒙版Image添加到Windows层。

使用方式：

//添加模糊效果

[SecurityStrategy addBlurEffect];

//移除模糊效果

[SecurityStrategy removeBlurEffect];

//配合AppDelegate中的方法,可方便集成的项目当中

//应用将失去激活状态---单击Home键

- (void)applicationWillResignActive:(UIApplication *)application

{

    //添加模糊效果

    [SecurityStrategy addBlurEffect];
    
}

//应用将变为激活状态----应用返回前台

- (void)applicationDidBecomeActive:(UIApplication *)application 

{

    //移除模糊效果
    
    [SecurityStrategy removeBlurEffect];
    
}

