# 内容生产流水线 Skill ✨

> 从资料到交付物：把网页、小红书、笔记、图片、视频、行程信息整理成经过检查的 PPT、攻略、文档或脚本。

`content-production-pipeline` 是一个内容交付型 Codex Skill。它不只是“写一段总结”，而是要求 Codex 走完整链路：**收集来源 → 结构化 → 去重 → 生成 → 检查 → 交付**。

## 适合什么场景？

- 旅行攻略：按天整理机票、住宿、游玩、现金和风险；
- 小红书调研：保留原链接、互动指标、可执行建议；
- PPT 制作：先搭结构，再放图片/链接，最后预览检查；
- 视频脚本：拆 hook、段落、画面、字幕和验收点；
- 教程文档：把零散资料变成别人能照着做的步骤。

## 为什么需要流水线？

内容任务最容易出现这些问题：

- 资料看了，但链接没留下；
- 内容生成了，但用户原始信息漏掉；
- PPT 做了，但没打开预览；
- 图片和排版看起来不对；
- 结论像总结，不能直接执行。

这个 Skill 的重点是“可交付”和“可检查”。

## 快速安装

```bash
git clone https://github.com/AuClarke/codex-skill-content-pipeline.git
ln -s "$PWD/codex-skill-content-pipeline/content-production-pipeline" ~/.codex/skills/content-production-pipeline
```

如果已经在仓库目录内：

```bash
ln -s "$PWD/content-production-pipeline" ~/.codex/skills/content-production-pipeline
```

## 如何触发

```text
Use $content-production-pipeline 把这些资料整理成一份可检查的 PPT。
```

或者：

```text
帮我把这段行程按天整理，保留费用、链接和检查项。
```

## 标准流程

1. **收集来源**：保留链接、文件名、截图或用户原文。
2. **结构化笔记**：按日期、主题、地点、事实、建议、风险整理。
3. **去重和标注不确定**：不要把猜测写成事实。
4. **生成交付物**：PPT、Markdown、脚本、表格或清单。
5. **检查交付物**：打开、预览、截图、检查链接或代表性内容。
6. **报告结果**：说明文件路径、检查动作和剩余风险。

## 交付验收清单

- 来源链接是否保留？
- 用户提供的每条信息是否都有去处？
- 是否标记不确定项？
- 排版/视觉是否实际检查？
- 链接是否抽查或统计？
- 文件是否保存到用户能找到的位置？

## 目录结构

```text
content-production-pipeline/
  SKILL.md
  agents/openai.yaml
  references/output-checks.md
```

## 和其它 Skill 怎么配合？

- 做 PPT：搭配 presentations skill；
- 做 Word 文档：搭配 documents skill；
- 学小红书：搭配 xiaohongshu-learning；
- 防跑偏：搭配 codex-guardrails；
- 大任务开始前：搭配 codex-task-kickoff。

## License

MIT
