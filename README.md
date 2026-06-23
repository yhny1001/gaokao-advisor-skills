# 高考志愿填报辅助 Skill

> 淋过雨的人，想给别人撑把伞。

## 缘起

高考填志愿是普通人一生中最重要的决策之一——一个选择可能影响 4-7 年的大学生涯，甚至 40 年的职业路径。但绝大多数考生和家长在面对这个决策时，信息极度不对称。

张雪峰老师在这件事上做了很多普及工作，他的方法论（城市>学校>专业、冲稳保、避坑天坑专业）非常有价值。但他把这套东西做成了付费生意，张口就是几千上万——**我是很不认可的。**

知识不应该垄断。所以我把这套方法论整理成了 AI Skill，免费开放，**任何考生和家长都能直接用。**

## 核心思想

**以 4-7 年长周期视角做决策。** 你今天报的专业，不是为你大一服务的，是为毕业那年服务的。任何行业都有周期——2016 年最火的土木，2020 年已开始收缩；2020 年大火的互联网运营，2024 年已大量裁员。永远用 4 年后的眼光看今天的选择。

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

### 方式二：直接复制 Prompt 模板（不需要 AI 工具）

**不需要任何 AI Skill 系统，不需要安装任何东西。**

打开你喜欢的任意 AI 工具（ChatGPT、Claude、DeepSeek、豆包、Kimi……），复制 [`prompt-template.md`](./prompt-template.md) 的完整内容，粘贴发送即可。AI 会自动扮演高考志愿填报顾问，按方法论标准流程给你建议。

👉 **[点击查看 Prompt 模板](./prompt-template.md)**

## 目录结构

```
gaokao-advisor/
├── SKILL.md              # 主 Skill 文件（AI Skill 系统用）
├── prompt-template.md    # 独立 Prompt 模板（复制发送给任意 AI 即可）
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

- 本 Skill 的方法论源自张雪峰老师公开的志愿填报观点，未采用其付费内容
- `references/` 中的数据来自 [gaokao-mentor-wisdom](https://github.com/dongsheng123132/gaokao-mentor-wisdom)（MIT License）
- 志愿填报涉及重大人生决策，本 Skill 提供方法论框架，具体选择请结合自身情况 + 最新数据
- **免费，永久免费。**
