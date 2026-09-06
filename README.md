# 每日AI财经新闻

一个每日 **08:00（北京时间）** 自动更新的「当日最新 AI 财经新闻」网页。

## 🌐 在线访问

**https://Drunk-101.github.io/daily-ai-news/**

每天 08:00 内容自动更新并同步到该网址，刷新即可查看最新一期。

## 文件说明

| 文件 | 作用 |
| --- | --- |
| `index.html` | 页面主体（样式、筛选、倒计时），打开即可浏览 |
| `news.js` | 当日新闻数据（`window.NEWS = { issue, items }`），每日更新重写此文件 |
| `README.md` | 本说明 |

## 本地预览

直接用浏览器打开 `index.html` 即可（数据在本地 `news.js` 中，无需联网）。

## 每日更新机制

页面内容通过 Codex 自动化任务维护：每天 **08:00（北京时间 Asia/Shanghai）** 自动运行一次，流程为：

1. 检索当日最新的 AI × 财经公开报道（财联社、东方财富、新华财经、腾讯财经早报、新浪财经、路透等）；
2. 筛选整理为若干条新闻（标题 + 摘要 + 来源链接 + 分类）；
3. 重写 `news.js` 中的 `issue`（期号日期）与 `items`（新闻条目），保持 `index.html` 结构不变；
4. `git commit` 并 `git push origin master`，自动同步到 GitHub Pages。

自动化任务可在 Codex 桌面端的「自动化 / 计划任务」中查看、暂停或修改运行时间。

## 部署（GitHub Pages）

- 仓库：https://github.com/Drunk-101/daily-ai-news （Public）
- 部署方式：Settings → Pages → Deploy from a branch（`master` / root）
- 代码推送到 `master` 后自动发布

## 注意事项

- 本页为个人资讯整理页，内容由 AI 自动搜集生成，可能存在滞后或误差，请以原始来源为准。
- 所载信息仅供参考，**不构成任何投资建议**。