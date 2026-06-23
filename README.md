# 高考志愿填报辅助 Skill

> 淋过雨的人，想给别人撑把伞。

## 缘起

高考填志愿是普通人一生中最重要的决策之一——一个选择可能影响 4-7 年的大学生涯，甚至 40 年的职业路径。但绝大多数考生和家长在面对这个决策时，信息极度不对称。

更残酷的是，**现在是 2026 年，AI 正在重塑整个就业市场。** 今天选的专业，毕业那年可能已经被 AI 替代了大半。过去的填报经验，很多已经失效——需要完全新的框架来思考这件事。

张雪峰老师在这件事上做了很多普及工作，他的方法论（城市>学校>专业、冲稳保、避坑天坑专业）非常有价值。但他把这套东西做成了付费生意，张口就是几千上万——**我是很不认可的。**

知识不应该垄断，特别是在这种关乎人命运的事情上。所以我把这套方法论升级后整理成了 AI Skill，**融入了 AI 浪潮冲击分析、宏观经济周期研判、4-7 年长周期决策框架**，免费开放给所有人。

## 核心思想

**以 4-7 年长周期视角做决策，以极其审慎的态度对待每一个建议。**

- 🧠 **AI 浪潮冲击**：按 🔴🟠🟡🟢 四级标注每个专业方向的 AI 替代风险
- 📈 **宏观周期研判**：人口老龄化、芯片自主化、能源转型、学历贬值……这些趋势直接决定 4 年后哪个方向有饭吃
- ⏳ **长周期视角**：2016 年最火的土木，2020 年已开始收缩；2020 年大火的互联网运营，2024 年已大量裁员。永远用 4 年后的眼光看今天
- 🛑 **反复追问机制**：AI 不会只凭一个分数就贸然给结论——必须收集到足够的个人情况后才给建议

张雪峰有对有不对的地方：方法论对，收费不对。这里取其精华，去其铜臭。

## 两种使用方式

### 方式一：安装为 AI Skill（推荐）

适合已在用 OpenClaw / Claude Code / Cursor 等 AI 工具的开发者或学生。

#### OpenClaw
将整个 `gaokao-advisor/` 目录放到 OpenClaw 的 skills 目录下（`~/.openclaw/workspace/skills/`），skill 自动加载。

#### Claude Code
将整个 `gaokao-advisor/` 目录放到 `.claude/skills/` 目录下：
```bash
git clone https://github.com/yhny1001/gaokao-advisor-skills.git
cp -r gaokao-advisor-skills/gaokao-advisor/ ~/.claude/skills/
```

#### Cursor / 其他
将 `SKILL.md` 内容作为自定义指令或系统 prompt 注入。

### 方式二：直接复制 Prompt 模板（不需要安装任何东西）

**零门槛。不需要任何 AI Skill 系统。**

打开 ChatGPT / Claude / DeepSeek / 豆包 / Kimi……复制 [`prompt-template.md`](./prompt-template.md) 全文，粘贴发送。AI 会自动扮演极其审慎的高考志愿顾问，按标准流程逐项收集你的信息后再给方案。

👉 **[点击查看 Prompt 模板](./prompt-template.md)**

## 目录结构

```
gaokao-advisor/
├── SKILL.md              # 主 Skill 文件（AI Skill 系统用）
├── prompt-template.md    # 独立 Prompt 模板（复制发给任意 AI）
├── references/           # 参考数据（105 条张雪峰结构化语录 JSON）
│   ├── zhuanye.json      # 专业选择 28 条
│   ├── jiuye.json        # 就业前景 18 条
│   ├── rensheng.json     # 人生哲理 18 条
│   ├── yuanxiao.json     # 院校推荐 16 条
│   ├── xuexi.json        # 学习建议 12 条
│   └── zhiyuan-celue.json # 志愿策略 13 条
├── README.md             # 本文件
└── LICENSE
```

## 声明

- 本 Skill 的方法论源自张雪峰老师公开的志愿填报观点，已做 AI 时代升级
- AI 就业冲击分析基于 2025-2026 年 LLM/Agent 发展现状外推
- `references/` 数据来自 [gaokao-mentor-wisdom](https://github.com/dongsheng123132/gaokao-mentor-wisdom)（MIT License）
- 志愿填报涉及重大人生决策，本 Skill 提供方法论框架，具体选择请结合自身情况 + 最新数据
- **免费，永久免费。**
