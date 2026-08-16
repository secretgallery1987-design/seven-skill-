---
name: structure-my-thinking-v1
description: Structure fragmented notes, voice-like thoughts, questions, judgments, or indecision into a traceable thinking model and actionable conclusion. Use when the user asks to clarify, organize, sort out, think through, define, or make sense of their own thinking. For consequential questions, first diagnose assumptions, missing information, and common reasoning errors, then ask exactly one decisive question and wait before producing the final structure.
---

# Structure My Thinking V1

## Protocol

1. Preserve the user's meaning and vocabulary. Do not improve away ambiguity that matters.
2. Decide whether the issue is consequential. Treat identity, career, business, money, relationships, health, or irreversible choices as consequential.
3. For a consequential issue, respond in two stages:
   - Stage 1: briefly state hidden assumptions, critical missing information and its impact, and likely reasoning errors; ask exactly one decisive question; stop.
   - Stage 2: only after the user's answer, produce the full structure below.
4. For a low-stakes issue with enough information, produce the full structure directly. Mark uncertain interpretations instead of inventing certainty.
5. Do not switch into knowledge extraction, content ideation, or workflow automation. Suggest the relevant separate skill only after this task is complete.

## Output

Use only sections that add information, while preserving this order:

1. 问题定义
2. 隐藏假设
3. 已知信息
4. 未知信息
5. 目标
6. 约束
7. 我的判断
8. 判断理由
9. 经验连接
10. 待验证项
11. 可行动结论

Label inferred content as `推测` and unresolved content as `待确认`. End with the smallest useful next action.

## Mobile-first behavior

Accept raw voice transcription, repetitions, fillers, and unfinished sentences without asking the user to reformat. Keep the first response short enough to answer easily on a phone. Preserve a compact summary that can be continued on desktop.

