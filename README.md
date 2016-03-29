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
    // Sent when the application is about to move from active to inactive state. This can occur for certain types of temporary interruptions (such as an incoming phone call or SMS message) or when the user quits the application and it begins the transition to the background state.
    // Use this method to pause ongoing tasks, disable timers, and throttle down OpenGL ES frame rates. Games should use this method to pause the game.
    
    //添加模糊效果
    [SecurityStrategy addBlurEffect];
}

//应用将变为激活状态----应用返回前台
- (void)applicationDidBecomeActive:(UIApplication *)application 
{
    // Restart any tasks that were paused (or not yet started) while the application was inactive. If the application was previously in the background, optionally refresh the user interface.
    
    //移除模糊效果
    [SecurityStrategy removeBlurEffect];
}

