# Gaokao Advisor Skill

高考志愿填报辅助 skill，基于张雪峰方法论。适用于 OpenClaw、Claude Code、Cursor 等 AI 工具。

## 安装

### OpenClaw
把 `gaokao-advisor/` 放到 OpenClaw 的 skills 目录下（如 `~/.openclaw/workspace/skills/`）。

### Claude Code
把 `gaokao-advisor/` 放到 Claude Code 的 skills 目录下（如 `~/.claude/skills/` 或 `.claude/skills/`）。

### Cursor / 其他 MCP 工具
将 `SKILL.md` 内容作为自定义指令或系统 prompt 注入。

## 目录结构

```
gaokao-advisor/
  SKILL.md              # 主 skill 文件（规则 + 方法论）
  references/           # 参考数据（可做 RAG 素材）
    zhuanye.json        # 专业选择语录（28条）
    jiuye.json          # 就业前景语录（18条）
    rensheng.json       # 人生哲理语录（18条）
    yuanxiao.json       # 院校推荐语录（16条）
    xuexi.json          # 学习建议语录（12条）
    zhiyuan-celue.json  # 志愿填报策略（13条）
  README.md             # 本文件
```

## 使用方式

触发后 AI 会自动走咨询流程，收集分数/位次/家庭条件等信息，然后给出填报建议。

核心功能：
- 城市/学校/专业优先级排序
- 黄金/白银/风险/天坑专业四象限分类
- 不同分数段和家庭条件的策略
- 冲-稳-保填报模板
- 十大避坑清单

## 数据来源

- 张雪峰抖音/直播公开内容
- 峰学蔚来公开方法论
- daxue.cn 高考志愿填报指南
- gaokao-mentor-wisdom（GitHub，MIT License）
