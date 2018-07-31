Xcode 错误总结
> The entitlements specified in application`s Code Signing Entitlements file do not match those specified in your provisioning profile

#### 解决方法
1. 重启
2. ProjectTarget and ProjectTests 的Development Team 不一样

参考：
<https://stackoverflow.com/questions/19581225/the-executable-gets-signed-with-invalid-entitlements-in-xcode>

