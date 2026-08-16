---
name: choose-personal-workflow-v1
description: Help the user choose among their five personal workflow skills when they send an unstructured thought, image, screenshot, article, PDF, viewpoint, experience, or task history without clearly specifying the desired processing. Use only as a lightweight intake selector: recommend one best-fit skill, or at most two when genuinely ambiguous, ask exactly one confirmation question in plain Chinese, and stop. Do not perform the selected skill's work or automatically chain skills.
---

# Choose Personal Workflow V1

## Selection protocol

1. Inspect the user's actual input and stated intent.
2. If the user explicitly names a Skill or clearly requests one defined outcome, do not intervene; let the matching professional Skill handle it.
3. If the intended outcome is unclear, select the most likely route:
   - untangle the user's own fragmented thinking → `$structure-my-thinking-v1`
   - extract an external source into a knowledge record → `$distill-knowledge-v1`
   - clarify or challenge the user's own position → `$calibrate-my-view-v1`
   - turn an existing idea or experience into content and assess asset potential → `$assetize-content-idea-v1`
   - analyze multiple task records for repeated work → `$discover-my-workflows-v1`
4. Ask exactly one short confirmation question using the Chinese task name. Mention the Skill name only as secondary help.
5. If two routes are genuinely plausible, present those two only and ask which outcome the user wants first.
6. Stop after the question. Do not execute, chain, or simulate the chosen Skill before the user confirms.
7. If none fits, answer normally; do not force a selection.

## Question patterns

Single route:

> 我判断这段内容最适合先做“结构化思考”。要现在这样处理吗？

Two routes:

> 这张图可以先“提炼知识入库”，也可以直接“发展内容与资产”。你想先做哪一个？

Keep the question easy to answer from a phone. Never require the user to memorize English names.

