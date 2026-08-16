# 第一阶段：个人创作认知工作流 Skills V1

这是一套由用户确认后调用的 5 个独立专业 Skill，另有 1 个只负责询问确认的轻量入口 Skill。五个专业模块共享结构化、可追溯、手机低摩擦的原则，但各自只完成一种任务。入口不执行专业工作，也不自动串联模块，因此当前版本仍不包含总控 Agent。

## 统一命名与目录

```text
phase-1-personal-workflow-skills/
├── README.md
└── skills/
    ├── structure-my-thinking-v1/
    ├── distill-knowledge-v1/
    ├── calibrate-my-view-v1/
    ├── assetize-content-idea-v1/
    ├── discover-my-workflows-v1/
    └── choose-personal-workflow-v1/
```

统一采用“动词 + 对象 + `-v1`”命名。每个目录中的 `SKILL.md` 是工作协议，`agents/openai.yaml` 是 Codex 的展示和默认调用信息。

当用户没有说明想怎样处理一段文字或图片时，`$choose-personal-workflow-v1` 只推荐最合适的方向并问一句确认问题。用户不需要记住其他 Skill 的英文名称。

## 选择哪一个

| 你的当前输入 | 调用 Skill | 它只负责什么 | 明确不负责什么 |
|---|---|---|---|
| 一段混乱想法或难题 | `$structure-my-thinking-v1` | 澄清问题并形成行动结论 | 提炼外部材料、做内容策划 |
| 视频、文章、截图、PDF 或他人观点 | `$distill-knowledge-v1` | 提炼来源并形成知识卡 | 猜你的态度、替你写成熟立场 |
| 你对某件事的反应或初步立场 | `$calibrate-my-view-v1` | 形成有边界的个人观点 | 总结整份素材、策划内容资产 |
| 已有观点、经历、知识卡或项目洞察 | `$assetize-content-idea-v1` | 变成聚焦选题并判断资产潜力 | 泛化生成爆款、虚构市场需求 |
| 一段时间的任务或对话记录 | `$discover-my-workflows-v1` | 找重复劳动和适合的标准化形式 | 在没有证据时声称发现规律 |

## 推荐组合顺序

组合不是强制流程，按当前需要只调用一个即可：

```text
外部素材 → 提炼知识 → 校准观点 → 内容资产化
碎片想法 → 结构化思考 → 校准观点 → 内容资产化
一段时间的真实记录 → 发现工作流 → 再决定是否单独做 Skill / 自动化
```

## 手机与电脑协作

- 手机端：直接粘贴或口述原始内容，并显式写 `$skill-name`。无需预整理。
- Skill 需要态度或关键判断时，只问一个问题，便于手机快速回答。
- 电脑端：把上一轮的结构化输出作为下一 Skill 的输入，或继续补充证据、来源和项目资料。
- 入库时保留来源、日期、标签和未验证项；可将各 Skill 的输出作为“个人创作认知库”的卡片正文。

## 真实调用示例

### 1. `$structure-my-thinking-v1`

- `$structure-my-thinking-v1 我最近一边想做 AI 内容，一边又觉得应该先把产品做出来。脑子很乱，帮我理清楚。`
- `$structure-my-thinking-v1 我口述一段关于是否离开当前合作项目的想法。先别急着给结论。`
- `$structure-my-thinking-v1 把这些零散笔记整理成我现在真正要解决的问题和下一步。`

### 2. `$distill-knowledge-v1`

- `$distill-knowledge-v1 提炼这个视频：作者说了什么、证据是什么，先问我对核心观点的态度再入库。`
- `$distill-knowledge-v1 阅读这份 PDF，为 AI 新手解释必要概念，并做成可追溯知识卡。`
- `$distill-knowledge-v1 这是三张文章截图。不要猜我是否认同，先找最值得我表态的观点。`

### 3. `$calibrate-my-view-v1`

- `$calibrate-my-view-v1 我觉得“普通人不需要学提示词”，但这句话可能太绝对。帮我校准。`
- `$calibrate-my-view-v1 从我下面这段反应里提炼我的真实观点，区分经验、事实和假设。`
- `$calibrate-my-view-v1 检查这个观点是否符合我“有经验的独立职业者重启”的长期定位，并指出可能误解。`

### 4. `$assetize-content-idea-v1`

- `$assetize-content-idea-v1 把“离开熟悉行业后，经验不会自动变成产品”做成一个选题，并判断能否沉淀为工具。`
- `$assetize-content-idea-v1 基于这张知识卡，给我一个最值得现在做的内容方向，不要给十个爆款标题。`
- `$assetize-content-idea-v1 这段客户经历适合文章、短视频还是清单？说明和未来产品的连接。`

### 5. `$discover-my-workflows-v1`

- `$discover-my-workflows-v1 分析我过去两周提供的任务记录，找重复步骤；没有证据的不要算。`
- `$discover-my-workflows-v1 这是 12 段我处理内容素材的对话，判断哪些适合做模板、Skill 或自动化。`
- `$discover-my-workflows-v1 根据这些操作日志估算重复劳动和节省时间；无法估算的字段请明确告诉我。`

## V1 测试方法

每个 Skill 先用上面的 2–3 个例子和真实材料各跑一次。记录：是否误触发、是否越界、是否问了多余问题、输出是否能直接成为下一步输入。累计 5–10 次真实使用后，再调整字段与边界。只有当跨 Skill 的调用顺序稳定、自动路由收益明确、错误路由风险可控时，才设计总控 Agent。

## 安装

将 `skills/` 下的五个文件夹复制到你的 Codex Skills 目录，然后重启或刷新 Codex。也可以先保留为项目内套件，用路径指定其中一个 Skill 做试运行。
