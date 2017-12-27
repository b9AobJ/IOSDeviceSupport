# IOSDeviceSupport
可用于高版本Xcode支持更低版本的IOS开发


### 注
Xcode 9默认不支持IOS 7了，但开发可能还未证实放弃这个系统，我们可以让Xcode默认也支持这个系统版本。

#### 1
将调试需要的配置文件拷贝出来，方法finder中前往文件夹/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport，例：需要支持iOS 7，将7.0和7.1文件夹拷贝。

#### 2
打开以下路径/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/ ，用Xcode打开SDKSettings.plist这个文件，加入如下图所示的配置，保存之后重启Xcode，之后在工程的Deployment Target里面就可以选择7.0了。注意：在修改SDKSettings.plist的文件时，直接用Xcode修改是没有权限修改的，建议使用其他编辑工具，个个人使用BBEdit修改的。