# App Stores — Current Gates

核对日期：2026-09-07。正式提交当天再次核对官方政策。

## Apple

官方 Enrollment：
https://developer.apple.com/help/account/membership/program-enrollment

当前官方事实：
- Apple Developer Program 年费 99 USD，地区可能显示本地货币；
- 个人/独资经营者以个人法定姓名作为 App Store seller；
- 组织账号需要合法实体；
- 组织验证要求 D‑U‑N‑S Number；
- 注册人需要能够代表组织签署法律协议；
- 工作邮箱需要关联组织域名；
- 组织网站需要公开、可用并与组织域名关联。

LinguaCafe 当前缺口：
- 选择个人还是组织账号；
- Apple Developer membership；
- macOS + 支持版本 Xcode；
- bundle/signing/provisioning；
- 当前源码真实 Xcode build；
- simulator / iPhone 验收；
- TestFlight；
- App Store Connect privacy；
- screenshots / metadata；
- review-safe account；
- App Review 结果。

源码和 Windows 静态检查不能替代这些证据。

## Google Play

官方 closed-test 要求：
https://support.google.com/googleplay/android-developer/answer/14151465

对 2023-11-13 以后创建的新个人开发者账号，Google 当前要求：
- production access 前进行 closed test；
- 至少 12 名 tester；
- 连续 opt-in 至少 14 天；
- 之后申请 production access；
- 申请时需要说明 tester engagement、feedback、App value proposition、production readiness。

这意味着“找 12 个真实测试者并让他们持续参与”本身就是发布项目，不只是点一下 Play Console。

### Account deletion

官方：
https://support.google.com/googleplay/android-developer/answer/13327111

如果 App 允许用户在 App 内创建账号，Google 当前要求：
- App 内提供删除账号及关联数据的路径；
- 同时提供一个网页资源，让用户可以请求账号及关联数据删除；
- Data Safety / deletion 信息会显示在商店页面。

因此 LinguaCafe 必须先冻结“移动端是否创建账号”。

如果移动端只登录既有服务器账号，仍要准确回答 Data Safety，并确认实际服务端删除流程和商店描述一致。

## Google Play current release path

至少包括：
- Play developer account；
- app record / package；
- current target API compliance；
- signed AAB；
- internal test；
- closed test（若账号规则要求）；
- tester feedback；
- pre-launch report；
- privacy policy；
- Data Safety；
- account deletion；
- content rating / target audience；
- store listing；
- production-access application；
- production review。

## LinguaCafe 的产品决定依赖

在商店投入大量工作以前，先决定：
1. 第一批用户是否需要原生 App，还是 Web/Android 先行；
2. iOS 是否值得立刻支付 Apple 账号和 macOS/Xcode 能力成本；
3. 移动端是否提供注册；
4. 服务器主要地区；
5. 免费/收费模式是否涉及商店内购规则。

## 发布成功证据

只有以下证据才算商店路线完成：
- 当前 commit 对应的 signed artifact；
- 真实设备/模拟器测试；
- 商店后台状态；
- reviewer/test account；
- privacy/deletion 页面；
- 实际审核结果。

旧截图、源码、API 200 或另一平台通过都不能替代。
