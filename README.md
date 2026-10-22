# think-and-grow-rich

把《思考致富》（拿破仑·希尔）里的**判断清单**变成一个能在一次对话里跑完的 Agent Skill：
明确目标 → 根因诊断 → 恐惧体检 → 自我分析 → 毅力处方 → 求职/推销服务 → 周复盘。

不是书摘，也不是鸡汤。它是一份**行为诊断流程**：先让用户说清目标，再用书里的清单反查他卡在哪一层，最后只给 3 个这周能验证的动作。

## 它解决什么问题

- 有目标但一直推不动（拖延 / 犹豫 / 反复重开）
- 想找工作、换行业、接单，但简历和沟通没打到点上
- 说不清自己要什么，想系统做一次自我审计
- 一遇失败就想放弃，或者总在等"恰当的时机"

## 安装

这是标准的 agent skill（`SKILL.md` + `references/` + `assets/`），三种用法：

**1. 放进 DeepSeek Harness / Claude Code 的技能目录**

```bash
# DeepSeek Harness
git clone https://github.com/Bobbychina/think-and-grow-rich.git ~/.dsh/skills/think-and-grow-rich

# Claude Code
git clone https://github.com/Bobbychina/think-and-grow-rich.git ~/.claude/skills/think-and-grow-rich
```

**2. 直接把本仓库当知识库**：把 `SKILL.md` 的内容喂给你的 agent，或让它按需读 `references/`。

**3. 自己照着用**：`assets/` 里有目标卡、诊断卡、周复盘三张表，打印或复制都能用。

## 结构

```
SKILL.md                     # 主流程（选模式、目标卡、诊断、恐惧、分析、处方、求职、复盘）
references/
  failure-causes.md          # 30 条失败原因 → 六层诊断 + 处方
  fears.md                   # 六种基本恐惧 + 担忧 + 犹豫
  self-analysis.md           # 59 题自我分析问卷（分组）
  persistence.md             # 毅力八要素 + 16 种缺乏表现
  job-hunt.md                # 简历六段 + 求职七步 + 试用期三问
  principles.md              # 核心判断与金句（纠偏用）
assets/
  goal-card.md               # 目标卡模板
  diagnosis-card.md          # 诊断卡模板
  weekly-review.md           # 周复盘模板
```

## 触发方式

```
用户：我这个项目拖了三个月了，每次打开就烦
agent：（加载 think-and-grow-rich）→ 模式 A → 目标卡 → 诊断卡 → 3 个动作
```

```
用户：帮我看看简历，投了 40 家没回音
agent：→ 模式 B → 简历六段检查 → 调研表 → 一页行动计划
```

```
用户：我好像一直不知道自己想要什么
agent：→ 模式 C → 先问一个目标问题 → 抽 10 题自我分析 → 3 缺点 + 补救
```

## 设计取舍

- **一次只做一层**：诊断不超过 5 条、行动不超过 3 件、问卷每轮不超过 10 题——这是为了防止"看完很爽、什么都不做"。
- **不可控项不进待办**：遗传、童年、年龄只标注，不让用户为改不了的事内耗。
- **不做心理治疗**：出现持续低落/成瘾/自伤议题，明确交回现实中的专业支持。
- **不承诺结果**：这是诊断书，不是致富保证。

## 版权说明

本仓库的方法论、清单结构与流程设计基于本人的读书笔记整理；引用原文仅作说明用途，版权归原作者及出版方所有。代码/模板部分（`assets/` 与流程设计）以 MIT 协议开放。

## License

MIT（见 [LICENSE](LICENSE)）
