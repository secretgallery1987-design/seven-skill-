---
name: distill-knowledge-v1
description: Distill a video, article, screenshot, PDF, transcript, or someone else's viewpoint into a traceable knowledge record for a personal creative knowledge base. Use when the user wants to understand, extract, summarize for reuse, connect, tag, or archive source material. Always separate the author's claims from the user's stance; never guess the user's attitude.
---

# Distill Knowledge V1

## Protocol

1. Identify the source and available evidence. If source content is inaccessible, request it or state the limitation; never reconstruct it from the title alone.
2. Extract what the author says, core claims, key support, reusable methods, and concepts an AI beginner needs to understand.
3. Distinguish direct source content from inference. Keep source locations, timestamps, page numbers, links, or quoted fragments when available.
4. Before recording a personal stance, ask exactly one highest-leverage attitude question by default. Offer the stance choices `认同 / 部分认同 / 反对 / 待验证`, tailored to the central claim. Stop and wait.
5. After the user answers, record their stance, why, experience relationship, existing-knowledge connections, emerging personal view, possible topics, and tags.
6. Do not turn the material into a polished personal position or full content plan. Hand those tasks to the separate calibration or assetization skill.

## Output

### 素材卡

- 来源与可追溯位置
- 作者说了什么
- 核心观点
- 关键论据与证据强度
- 值得保留的方法
- AI 新手需理解的概念
- 不确定或待核实之处

### 我的认知卡

- 我的态度：认同 / 部分认同 / 反对 / 待验证
- 为什么
- 与我的经验的关系
- 与已有知识的连接
- 可形成的个人观点
- 可发展选题
- 标签

Omit `我的认知卡` until the user supplies their attitude. Use explicit `未提供` values rather than guessing.

