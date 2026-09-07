# Current Status — 2026-09-07

## Product

- 产品定位已相对清楚：真实阅读 + WordSense + sense-only FSRS。
- 新精简产品计划已经把首页、阅读、复习、生词、我的作为日常主体验方向。
- 真题/我的材料、有限离线和移动端是后续真实用户价值的重要组成部分。

## Release

- Web/PC：实现最完整，但需要当前版本重新验收。
- Android：实现存在；生产发布和 Play Console 状态待确认。
- iOS：实现存在；最终 Xcode/签名/设备/TestFlight/App Store 证据不完整。
- 服务器：已有云端主导架构设计，但真实公开生产部署尚未在本仓形成完成证据。

## Operations / business

当前文档资产偏技术，以下领域需要从零或近似从零建立：
- 用户支持；
- 公开状态页；
- onboarding；
- 真实用户测试；
- 宣传渠道；
- 内容增长；
- 定价；
- 支付；
- 商业模式；
- 投资人材料；
- 真实留存和转化数据。

## Public security

三个公开仓的 GitHub Secret Scanning 和 Push Protection 已于 2026-09-07 开启。
源码仓仍有公开卫生问题待修，因此当前不应继续无筛选地公开推送本地工作区内容。
