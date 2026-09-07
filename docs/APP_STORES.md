# App Stores

## Apple

当前官方事实（2026-09 查询）：
- Apple Developer Program 当前为 99 USD / membership year，地区可能显示本地货币。
- 组织账号需要满足 Apple 的组织验证要求；Apple 官方说明组织通常需要 D-U-N-S Number、组织域名邮箱和公开网站。
- TestFlight、签名、App Store Connect 和真实设备/模拟器证据必须在 macOS/Xcode/Apple 账号能力中完成。

LinguaCafe 当前：
- iOS 源码和上架材料存在。
- 最终 Xcode build、签名、TestFlight、App Store Review 未完成。
- 不得从 Windows 源码推断“iOS 已可发布”。

官方参考：
https://developer.apple.com/programs/enroll/
https://developer.apple.com/help/account/membership/program-enrollment

## Google Play

当前官方事实：
- Google Play 要求 Data Safety 与隐私政策保持一致。
- 如果 App 内允许创建账号，Google Play 要求 App 内和外部网页都提供账户删除请求入口。
- Google Play 提供 internal / closed / open testing；生产发布前应按当前账户类型和 Play Console 要求完成测试。
- 2026-09-30 起 Play Console 有更新后的开发者验证/注册要求，需要发布前再次核对。

官方参考：
https://support.google.com/googleplay/android-developer/answer/10144311
https://support.google.com/googleplay/android-developer/answer/13327111
https://support.google.com/googleplay/android-developer/answer/9845334
https://support.google.com/googleplay/android-developer/answer/17125096

## LinguaCafe 的具体 Gate

- 是否在移动端创建账号，会直接影响商店账户删除设计。
- 隐私政策必须有稳定公开 HTTPS URL。
- Store listing、截图、review account、测试数据都要和真实生产行为一致。
