---
name: discover-my-workflows-v1
description: Analyze a supplied period of task records, conversations, files, or operating notes to discover repeated work the user may not notice. Use when the user asks what they repeat, what to standardize, automate, turn into a Skill, or eventually delegate to an Agent. Require evidence and never claim observation of data that was not provided or inspected.
---

# Discover My Workflows V1

## Evidence rules

1. Define the observation window and inspected sources before making claims.
2. Distinguish `observed`, `user-reported`, and `inferred` evidence.
3. Cite concrete examples with dates, task names, file paths, or conversation snippets when available.
4. Do not convert one occurrence into a repeated pattern. Use `candidate pattern` when frequency is unknown or fewer than two instances are observed.
5. State coverage gaps. Never imply access to the user's whole history.

## Analysis

1. Normalize activities into trigger, input, steps, decision points, output, tools, and handoffs.
2. Cluster similar sequences while preserving meaningful differences.
3. Estimate frequency only from the inspected sample; state the denominator and confidence.
4. Locate repeated manual transformations, recurring questions, bottlenecks, error-prone steps, and approval points.
5. Classify the best intervention:
   - checklist/template: stable steps, human judgment remains central
   - Skill: repeatable bounded capability with variable inputs
   - automation: deterministic trigger and action with low ambiguity
   - Agent candidate: multi-step routing and judgment across capabilities; recommend only after component workflows are proven
6. Estimate time savings as a range based on stated or observed duration. If duration is absent, write `无法估算` and name the missing data.
7. Prioritize by frequency, time cost, standardizability, error reduction, strategic value, and risk.

## Output

- 分析范围与证据覆盖
- 重复模式：name, trigger, evidence, observed frequency, confidence
- 可标准化步骤
- 适合形式：模板 / Skill / 自动化 / Agent 候选, with rationale
- 预计节省时间：range and assumptions, or `无法估算`
- 风险与必须保留的人类判断
- 建议优先级：现在 / 稍后 / 暂不做
- 下一次应记录的数据

Do not build the recommended system unless the user separately asks for implementation.

