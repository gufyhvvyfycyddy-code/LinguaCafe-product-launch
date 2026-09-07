# Review Start Here

## 1. 产品是什么

LinguaCafe 面向希望通过真实英语材料学习的人。用户在句子里学习具体 WordSense，自然阅读参与记忆强化，FSRS 补上自然阅读未覆盖的复习。

产品体验借鉴：
- 墨墨 / MaiMemo：每日任务清楚、主流程少、打卡和连续学习感。
- Anki：FSRS、Question → Show Answer → Again/Hard/Good/Easy、历史和可解释调度。

LinguaCafe 自己的差异：
- 学习单位是具体词义，不是单词字符串；
- 原文来源和例句是学习证据；
- 阅读和复习是一条学习链；
- AI 主要辅助解释、翻译和消歧。

## 2. 当前上线状态

- 源码已公开，但公开安全卫生仍有 P0 待处理。
- Web/PC 功能最完整；冻结基线 `6989ed27c933716f9069bb9b14fba92624081fc4` 已完成 Reader → WordSense → sense Review 主链的真实 Chrome 验收，并验证正式 Docker 镜像加载原生 FSRS。当前源码 `master` 已继续完成安全和依赖收口至 `2abc82df754525c19733382200aaf72a930d436a`；当前 CodeQL 0 open，Dependabot 28 open（0 Critical / 6 High / 18 Medium / 4 Low），6 个 High 已有逐项证据处置。后续源码事实与冻结浏览器验收范围分开理解。
- Android 工程存在，Play Store readiness 未重新验证。
- iOS 工程和上架材料存在，但 macOS/Xcode/签名/TestFlight/App Store 仍是外部能力 Gate。
- 还没有完成面向真实用户的服务器部署、公开测试、增长和商业验证闭环。

## 3. 希望外部审查者回答

- 第一批用户应该是谁？
- 首发应该先 Web、Android，还是同时准备 iOS？
- 服务器最低可用方案是什么？
- 隐私、账号删除、客服和备份还缺什么？
- 哪些渠道最适合获得前 10、50、100 个真实用户？
- 哪些宣传内容能体现产品价值，而不是只展示“AI 写了一个 App”？
- 什么数据达到什么程度后才值得收费或找投资人？
