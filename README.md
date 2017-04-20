# Native messaging in Microsoft Edge


## Firstly
* Please upgrade windows 10 to Version 1703

> [Download Site](https://www.microsoft.com/zh-cn/software-download/windows10)

## Note
1. extension和UWP之间的在同一进程中通讯流程已经走通.
2. Package.appxmanifest need to add `<Extensions>`

## Audio & Video
* 目前仅仅是extension和UWP之间的通讯，UWP调用其他应用服务需要重写NativeMessageingHostInProcess下App.xaml.cs中的逻辑.
* 集成audio/video应该需要参考[Adding a Desktop Bridge component](https://docs.microsoft.com/zh-cn/microsoft-edge/extensions/guides/native-messaging#desktop-bridge-component) and [Desktop to UWP Bridge](https://docs.microsoft.com/en-us/windows/uwp/porting/desktop-to-uwp-root)

## Build Steps
1. build and deploy meetExtensionHostInProcess
2. copy Extension to bin\x86\debug\Appx
3. deploy meetExtensionHostInProcess

## Test

* open http://*/secureinput.html


