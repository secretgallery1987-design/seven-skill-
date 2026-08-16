---
name: choose-personal-workflow-v1
description: Act as a lightweight discovery and confirmation layer for the user's installed personal Skills. Use when the user sends an unstructured thought, image, screenshot, article, PDF, experience, content idea, research request, or task history without naming a Skill or making the desired outcome clear. Inspect the currently available personal Skills, including the five cognition workflow Skills and content-strategy-radar. When one route is clearly implied, invoke it and briefly tell the user; when two outcomes are plausible, recommend at most two in plain Chinese, ask exactly one confirmation question, and stop. Do not require Skill names, force a Skill onto ordinary questions, or automatically chain multiple Skills.
---

# Choose Personal Workflow V1

## Discovery protocol

1. Inspect the current available-skills catalog instead of relying only on a fixed list. Consider personal and domain-specific Skills before generic capabilities.
2. Do not intervene when the user explicitly names a Skill.
3. If the user clearly requests one outcome that matches one Skill, use that Skill directly and state the choice in one short sentence.
4. If the input is raw and its desired outcome is ambiguous, recommend the one most likely route. If two routes are genuinely plausible, present two only.
5. Ask exactly one confirmation question in Chinese and stop. Do not execute either route until the user answers.
6. Use human task names first; show `$skill-name` only as optional reference. Never require memorization.
7. Do not propose a chain of Skills unless the user separately asks for a workflow. Select the first useful step only.
8. If no installed personal Skill fits, answer normally. Do not force selection.

## Current personal routes

Prioritize this registry, while still checking newly installed Skills:

- 整理零碎想法、澄清难题 → `$structure-my-thinking-v1`
- 提炼文章、视频、图片或 PDF 并进入认知库 → `$distill-knowledge-v1`
- 形成、挑战或校准个人观点 → `$calibrate-my-view-v1`
- 把已有观点或经历发展成内容与产品资产 → `$assetize-content-idea-v1`
- 从多条任务或对话记录发现重复工作流 → `$discover-my-workflows-v1`
- 研究内容信号、验证方向、生成经批准的选题或制作方案 → `$content-strategy-radar`

Treat lower-level supporting Skills such as Xiaohongshu retrieval as implementation details unless the user explicitly asks for a platform action.

## Examples

Clear route:

> 这是一段外部文章，我会用“提炼知识入库”处理，并先请你确认对核心观点的态度。

Ambiguous route:

> 这段经历可以先“整理成你的真实观点”，也可以直接“发展成内容资产”。你想先做哪一个？

Content radar:

> 你是在找最近值得研究的内容信号，我建议启动“内容雷达”。要先跑研究阶段吗？

Keep every selector interaction easy to answer from a phone.

