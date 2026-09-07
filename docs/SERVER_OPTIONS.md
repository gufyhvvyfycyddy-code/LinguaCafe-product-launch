# Server Options — First Real Users

状态：候选方案，不是采购单。

## 原则

前 10–100 个真实用户先使用最小可恢复架构。

必须做到：
- 用户数据隔离；
- HTTPS；
- 自动备份；
- 真实恢复演练；
- 邮件；
- 错误/可用性观察；
- 失败部署可以回滚。

当前没有证据需要 Kubernetes、微服务、多地域复制或复杂 CDN。

## 候选 A：一台小型 Linux VM

适合：
- 封闭测试；
- Laravel；
- 小规模数据库；
- queue / cron / tokenizer；
- reverse proxy + HTTPS。

DigitalOcean 官方价格，2026-09-07 核对：
https://www.digitalocean.com/pricing/droplets

示例：
- 1 GiB / 1 vCPU：USD 6/月；
- 2 GiB / 1 vCPU：USD 12/月；
- 2 GiB / 2 vCPU：USD 18/月；
- 4 GiB / 2 vCPU：USD 24/月。

LinguaCafe 同时存在 Laravel、数据库、队列和 tokenizer。2 GiB 可作为第一轮压测起点，但不能直接当成最终配置。

## 异地备份 / 对象存储候选

Cloudflare R2 官方价格：
https://developers.cloudflare.com/r2/pricing/

2026-09-07 核对：
- Standard storage：USD 0.015 / GB-month；
- Class A：USD 4.50 / 百万次；
- Class B：USD 0.36 / 百万次；
- Standard egress：无带宽出口费。

可能用途：
- 加密的异地备份；
- 未来媒体/附件对象存储。

没有真实容量压力前，不提前迁移全部媒体。

## 邮件候选

Resend：
https://resend.com/pricing/

2026-09-07：
- Free：3,000 封/月，100 封/日；
- Pro：USD 20/月，50,000 封/月。

早期封闭测试可以先用免费层验证注册/找回密码流量是否足够。

## 可用性监控候选

Uptime Kuma：
https://github.com/louislam/uptime-kuma

可以监测：
- HTTP/TCP/DNS；
- HTTPS 证书；
- 状态页；
- 通知。

重要服务的监控最好不要和唯一生产服务器放在同一个故障点。

## 第一版建议拓扑

Domain + HTTPS → 单一应用 VM → Laravel + DB + queue/tokenizer

另加：
- 加密异地备份；
- transactional email；
- 外部 uptime check；
- GitHub security checks。

## 先决定服务器地区

租长期服务器前先决定主要用户和发布区域：
- 中国大陆；
- 香港 / 新加坡 / 日本；
- 欧洲；
- 其他海外地区。

地区会影响：
- 延迟；
- 备案和合规；
- 支付；
- 商店；
- 用户获取。

## 成本规则

只把公开价格当作当日参考。正式采购重新核价。

完整成本还要算：
- 域名；
- 备份；
- 邮件；
- 监控；
- 存储/流量；
- Apple/Google 开发者费用；
- 支付费率；
- 客服；
- 税务/公司成本；
- 未来若托管 AI 的模型费用。
