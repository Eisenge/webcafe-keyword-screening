---
name: webcafe-keyword-screening
description: 每日刷 Web.Cafe（哥飞）词库选词决策的总入口。用于：①每日扫描哥飞新词/二次爆火/长青词库判断哪些关键词值得做（独立站 or 内页）；②核查哥飞 AI（new.web.cafe/chat）对候选词的社群意见；③记录筛选结论与排除关键词台账；④为出海工具站/游戏站/内容站选主词与长尾词。触发词包括"刷哥飞词库/今日新词/哪些词可以做/哥飞建议/选词/关键词筛选/排除关键词"。所有判断须独立核对哥飞词库数据 + 真实 Google SERP + 哥飞 AI 意见，不得让 AI 凭空编词。
---

# Web.Cafe 词库每日筛选与选词决策

在运营多个出海站（noomicheems 游戏站、krillion 每日问答站、工具站）的背景下，每天从哥飞词库挑出可落地的关键词（新站首页 / 内页 / 新闻页），并记录排除理由。本项目所有筛选结论、哥飞原话建议、排除关键词台账都在 references 里，先读再筛。

## 开始之前

1. 读 [references/keyword-ledger.md](references/keyword-ledger.md) —— 已有结论与排除词，防止重复推荐用户已否的方向。
2. 读 [references/gekefei-advice.md](references/gekefei-advice.md) —— 哥飞对格式转换老词、品牌词/商标词等品类的明确态度（这两类已判死，不要重新推荐）。
3. 读 [references/gekefei-methodology.md](references/gekefei-methodology.md) —— 筛选方法与上站运营 SOP。

## 每日筛选流程

1. **扫数据源**（浏览器 Use 打开）：
   - 新词/更新批次：https://new.web.cafe/data/updates
   - 二次爆火：https://new.web.cafe/keywords?tab=resurgence
   - 长青词库（worth 过滤）：https://new.web.cafe/keywords?tab=evergreen&v=worth
   - 单个词详情：https://new.web.cafe/keywords/<slug>
2. **按判定标准筛**（gekefei-methodology.md §筛选标准）：热度(GPTs×)、趋势、竞争度（前两页是否大站内页/有无独立首页）、意图（真实 Google SERP 验证）、与现有站点契合度、用户已否方向。
3. **存疑词查哥飞 AI**：https://new.web.cafe/chat 提问（问清"社群怎么看 / 差异化 / 变现 / 有无案例"，要求给可核对帖子标题，不编造），等待"查找中/提取证据中"消失后读全文。
4. **更新台账**：把当日结论写进 keyword-ledger.md（值得做 / 可以试试 / 不值得做 + 原因）。

## 硬性红线（已获哥飞原话确认，不得重新推荐）

- **格式转换类老词**（PDF/PPT/Word/图片/视频/音频格式互转）：哥飞 2026-08-05 明确"都不适合新站去做"；含 excel to pdf、word to pdf、pdf to word、convertir pdf a word。
- **品牌词/商标词**（项目名、大厂产品名、含注册商标的短语如 "Photoshop"）：哥飞明示不推荐注册品牌词域名，社群有被起诉索赔数百万、域名被没收、收 DMCA 的案例。
- **用户已否方向**（见 keyword-ledger.md）：下载器类（IG reels/YouTube/MP3）、celebrity AI 声音、AI baby/logo 生成器、windsurf-cam、多合一工具站、AI 图片编辑主词。
- **盗版内容词**：如 haiku movie download，不做。

## 输出与交付

- 每日筛选结论更新 keyword-ledger.md，标注日期与批次。
- 推荐候选词必须附：GPTs× 数值、KD/月搜、前两页竞争结构、真实 SERP 意图验证、建议落地形态（新站/内页）。
- 与用户沟通用中文；网页内容语言随站点目标市场。

## 证据与完成度

- 词库页判定卡与哥飞 AI 意见不一致时，以哥飞本人原话/社群实证为准（如 excel to pdf 词库判"值得做"但哥飞劝退，最终听哥飞）。
- 判定"值得做"≠保证排名/收入；区分"哥飞判定"、"哥飞本人意见"、"社群案例实证"三个口径。
- 哥飞 AI 未给出完整 URL 时，记录可核对的帖子标题即可，不编造链接。
