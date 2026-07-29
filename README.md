# 游戏开发周刊 · Dev Weekly

Unity / AI 工作流 / 独立游戏市场，每周一期。

- 最新一期：<https://tang-xiaolong.github.io/weekly-site/>
- 往期归档：<https://tang-xiaolong.github.io/weekly-site/archive.html>
- RSS 订阅：<https://tang-xiaolong.github.io/weekly-site/feed.xml>

## 这是怎么做出来的

本仓是纯静态产物，由私人助理引擎（[PersonalAssistant](https://github.com/tang-xiaolong/PersonalAssistant)
的 `dev_weekly` 管道）每周一自动出刊：

```
采集(Python)  RSS / GitHub API / Reddit 周热帖 / HN
   ↓
去重(Python)  URL 规范化 → 标题词集合判同 → 跨期永久账本（同一条只会出现一次）
   ↓
选稿(AI)      在候选清单里挑选、归类、写中文点评（只能引用候选 id，不能编造链接）
   ↓
发布(Python)  data/issues/NNN.json → 渲染 HTML/RSS → git push（GitHub Pages）
```

`data/issues/*.json` 是每期的真相源，页面只是它的投影——改样式重渲染即可，历史内容不变。

## 声明

- 条目均来自公开 RSS / API，本刊只收录**标题、原文链接与本刊点评**，不转载原文正文，版权归原作者所有。
- 点评由 AI 辅助生成、不逐条人工复核，不代表原作者观点；发现错漏欢迎开 issue。
