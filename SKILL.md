---
name: structure-my-thinking
description: Structure a user's fragmented thinking through a low-friction two-stage dialogue. Use when the user sends scattered notes, half-formed ideas, voice-transcription-like fragments, or asks to clarify, sort out, think through, define, judge, or turn their thoughts into an actionable conclusion. First diagnose hidden assumptions, missing critical information and its impact, and common reasoning errors; then ask exactly one decisive question. Only after the user answers, distinguish facts, opinions, assumptions, experiences, goals, constraints, and items to verify, and compress the thinking into problem definition, knowns, unknowns, judgment, reasons, experience connections, and actionable conclusions.
---

# Structure My Thinking

Turn rough input into clear thinking without making the user prepare or format it first. Accept short text, long dumps, mixed fragments, and imperfect voice transcription in Chinese or the user's language.

## Preserve the two-stage contract

Track whether the current exchange is in Stage 1 or Stage 2.

### Stage 1: Diagnose and ask

On the first input:

1. Infer the question the user appears to be working on. Do not silently treat the inference as fact.
2. Identify internally:
   - hidden assumptions;
   - missing critical information and how each gap could change the conclusion;
   - likely reasoning errors, such as confusing preference with fact, jumping from one experience to a general rule, false either-or choices, unclear success criteria, or solving before defining the problem.
3. Select the single missing answer with the greatest expected impact on the direction, standard, or action.
4. Reply briefly with:
   - a one-sentence provisional reading of what the user is trying to decide;
   - only the most consequential assumption, information gap, or likely error, stated without lecturing;
   - exactly one question.

Do not provide the final structure, a list of questions, solutions, content ideas, or a polished rewrite in Stage 1. Do not ask the user to fill in a template. A question with several subquestions joined together still violates the one-question rule.

If the user's goal is already explicit, ask for the decisive criterion, constraint, or evidence—not for information already provided. If the input is extremely thin, ask what decision or outcome they want this thinking to support.

### Stage 2: Structure after the answer

Treat the user's next substantive reply as the answer to the decisive question. Integrate it with the original fragments and produce the structure below. Do not restart Stage 1 merely because some uncertainty remains. Ask another question only when proceeding would create a materially misleading result; otherwise mark uncertainty under `待验证`.

## Classify claims before synthesizing

Use these meanings:

- `事实`: externally checkable or directly observable information. Do not upgrade an unsupported claim to fact.
- `观点`: an interpretation, preference, evaluation, or position.
- `假设`: something currently treated as true so reasoning can proceed.
- `经验`: a personal event, repeated observation, or lesson reported by the user.
- `目标`: the desired change, decision, or outcome.
- `约束`: a limit on time, money, ability, identity, risk, resources, or acceptable methods.
- `待验证`: a claim or unknown that could materially alter the judgment.

When one sentence contains several types, split it. Preserve the user's intended meaning and voice. Never invent supporting facts, motives, or experiences. Label inference explicitly.

## Produce the Stage 2 output

Adapt length to the input. Prefer compact bullets that read well on a phone.

### 思考结构

**问题定义**  
One precise sentence describing the real decision or problem, including the desired outcome when known.

**已知**  
Group only categories that contain useful material: 事实、观点、假设、经验、目标、约束.

**未知 / 待验证**  
List only uncertainties that could change the judgment or next action. State their impact when it is not obvious.

**当前判断**  
Give the clearest conclusion supported now. Calibrate confidence; distinguish the user's judgment from Codex's inference.

**理由**  
Show the short reasoning chain. Note any assumption on which the judgment depends.

**经验连接**  
Connect the judgment to the user's stated experience. If none was provided, write `暂无足够的经验信息，不强行连接。`

**可行动结论**  
Give one smallest meaningful next action. Optionally add one decision rule or verification step when essential. Avoid turning this into a large plan unless requested.

End with a one-sentence compressed takeaway that the user could save or reuse.

## Keep interaction low-friction

- Accept raw fragments without correcting spelling or asking for reformatting.
- Respond in the user's language; default to concise Chinese for Chinese input.
- Make Stage 1 short enough to answer from a phone in one message.
- Let answers such as `是`, `不是`, a number, or one sentence be sufficient when possible.
- Carry context across devices within the same task; do not ask the user to paste the original fragments again.
- If the user explicitly requests `直接整理` or says not to ask questions, honor that request: make the key assumption explicit and proceed to Stage 2.
- If the user explicitly wants brainstorming rather than clarification, use this workflow only when unclear thinking blocks useful brainstorming.

## Examples

Input: `我想做AI内容，但又怕变成教工具的。我以前做摄影很多年，也不想总讲过去。现在是不是该做个人IP？`

Stage 1 response: `你真正要决定的，可能不是“要不要做个人IP”，而是未来内容应围绕哪种长期价值展开。目前最关键的缺口是：你希望这个账号最终带来什么结果？`

After the user answers, produce the complete Stage 2 structure.

Input: `直接整理：这个产品有人问，但没人买，我觉得可能定价太高。`

Skip the question, label `定价太高` as an assumption, note missing conversion evidence under `待验证`, and proceed to Stage 2.
