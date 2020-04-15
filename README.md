# umpush

友盟推送的 flutter 插件，使用帐号测试都是可用的。

# 包括的功能

1. 友盟推送：支持小米、华为、魅族的离线唤醒功能，亲测可用。从友盟后台推送的时候，需要勾选“MIUI、EMUI、Flyme 系统设备离线转为系统下发”，填写打开指定页面是：com.via.umpush.UmengOtherPushActivity

3. 由于基于项目，不需要 tags，我们只需要根据推送的 url 跳转到指定的界面而已，很多功能我没封装。

# 安卓平台需要注意一下

1. so 文件只能使用 armeabi-v7a

```
   ndk {
        moduleName "app"
        abiFilters 'armeabi-v7a'//,'armeabi','arm64-v8a'
   }
```

2. 仿照 example/android/app/AndroidManifest.xml，把友盟帐号填写上去；

3. 必要的时候修改一下安卓 AndroidManifest.xml 的包名和 build.gradle 里面的 aplicationId，

4. 离线唤醒  需要申请小米、华为、魅族的帐号，请严格参考这个文档进行：https://developer.umeng.com/docs/66632/detail/66744#h1--push-6
   有不懂就问他们的在线客服吧
