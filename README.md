# 小红书知识图解 Skill

一个面向 AI 小白的小红书知识卡片工作流：从选题、联网核验和术语消歧开始，设计故事化分页，在用户确认后生成统一的 3:4 手绘白板风格图文，并逐张验收。

## 能做什么

- 从关键词、长文、文件或截图中筛选一个适合传播的知识主题
- 用可信来源交叉核验定义、机制、边界与常见误区
- 生成至少 4 页的故事板，并在出图前等待用户确认
- 统一封面、角标、配色、纸张质感与角色设定
- 交付标题、200 字内正文、成组图片与来源链接

## 安装

克隆仓库后，将 skill 目录复制到 Codex 的 skills 目录：

```bash
git clone https://github.com/o2925960-cpu/xiaohongshu-knowledge-cards.git
mkdir -p ~/.codex/skills
cp -R xiaohongshu-knowledge-cards/.agents/skills/xiaohongshu-knowledge-cards ~/.codex/skills/
```

重新启动 Codex 后，可以这样使用：

```text
使用 $xiaohongshu-knowledge-cards 分析“RAG”，先提出选题和页数方案，等我确认后再生成图文。
```

## 目录

```text
.agents/skills/xiaohongshu-knowledge-cards/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── research-and-story.md
    └── visual-system.md
```

## 设计说明

这个 skill 把“研究与策划”和“生成与验收”明确分开。它不会在没有核验事实、确认页数和批准故事板的情况下直接批量出图。

仓库不包含来源不明的第三方视觉参考图；视觉方向以文字规范描述，避免开源分发中的版权风险。

## License

[MIT](LICENSE)
