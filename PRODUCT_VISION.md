# Product Vision

## Goal

LinguaCafe 要把这条学习链做成普通用户可以长期坚持的产品：

真实阅读 → 发现不懂的词/词组 → 确认具体 WordSense → 回到原文 → FSRS 在需要时补复习

最终目标看四件事：
- 用户愿意持续读；
- 用户不用花大量时间整理卡片；
- 用户知道今天该做什么；
- 学习记录可靠，阅读和复习共享同一套学习对象。

## 已有产品原则

1. 正式学习内容是具体 WordSense。
2. Sense ReviewCard 是正式 FSRS 调度对象。
3. 原文 occurrence 是学习证据。
4. ReviewLog 只记录真实评分。
5. AI 主要帮助解释、翻译、候选和消歧，不自动伪造学习历史。
6. 高级工程信息退到次级入口。
7. 首页优先告诉普通用户“今天做什么”。

## 从 Anki 借鉴什么

官方材料：
- https://docs.ankiweb.net/
- https://docs.ankiweb.net/deck-options

借鉴：
- FSRS；
- Question → Show Answer → rating；
- Again / Hard / Good / Easy 语义；
- review history 与调度可解释性；
- 内容对象和调度对象分离。

不照搬：
- 通用 Note Type / Card Template；
- 任意层级 deck 树；
- 默认 sibling cards；
- Anki 式完整本地 collection 权威。

## 从墨墨 / MaiMemo 借鉴什么

官方材料：
- https://www.maimemo.com/
- https://memodocs.maimemo.com/docs/memo/

可借鉴：
- 每日任务简单；
- 内容简洁；
- 复习有针对性；
- 数据一目了然；
- 高级设置存在，但不支配日常路径。

LinguaCafe 不直接复制墨墨的单词上限或具体商业模型。

## 为什么值得做真实用户测试

社区经验反复出现两个痛点：

- 阅读时制作卡片会打断阅读，流程很慢：
  https://www.reddit.com/r/Anki/comments/d8nsjs/
- 高阶学习者认为制作细致词汇卡很耗时：
  https://www.reddit.com/r/languagelearning/comments/1d4mx2j/
- 2026 年仍有 Anki 用户说做卡时间接近学习时间：
  https://www.reddit.com/r/Anki/comments/1v302ds/
- 近期用户仍希望把上下文直接带进词汇卡：
  https://www.reddit.com/r/Anki/comments/1re9jti/

这些只是社区体验，不等于 LinguaCafe 已证明 product-market fit。

## 必须用真实用户回答的问题

- 普通用户能否理解“具体词义”而不需要理解 WordSense 术语？
- 自动保留语境是否真的减少做卡成本？
- 用户读完以后会不会回来复习？
- 每日首页能否帮助坚持？
- LinguaCafe 是否比“词典 + 笔记 + Anki”更省事？
- 哪一类用户愿意连续用几周？
