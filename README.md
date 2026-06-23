# Learning Assistant Builder Skill Low

这是一个可通过 GitHub 链接安装的 Codex Skill，同时包含可复制到其他 Agent 工具中的通用提示词版本。

这个版本的流程更短：问答交流完成后会直接生成设计文档，不再额外确认使用逻辑或确认是否生成文档；用户确认设计文档后再开始生成产品。

同时加入轻量界面设计质量控制：在不改变问答流程、Vite 自动端口启动和快速 MVP 目标的前提下，让学习辅助类 Web 应用更美观、更有产品感、更适合课堂展示，并减少学生作品同质化。

## GitHub 安装链接格式

把本仓库上传到 GitHub 后，Skill 安装链接应使用下面这种格式：

```text
https://github.com/<你的GitHub用户名>/learning-assistant-builder-skill-low/tree/main/skills/learning-assistant-builder
```

例如：

```text
https://github.com/your-name/learning-assistant-builder-skill-low/tree/main/skills/learning-assistant-builder
```

## 在 Codex 中安装

### 推荐：使用通用 Skills CLI

安装到 Codex：

```bash
npx -y skills add Nagi1998/learning-assistant-builder-skill-low --skill learning-assistant-builder --agent codex
```

安装到 Claude Code：

```bash
npx -y skills add Nagi1998/learning-assistant-builder-skill-low --skill learning-assistant-builder --agent claude-code
```

安装到当前工具自动检测到的 Agent：

```bash
npx -y skills add Nagi1998/learning-assistant-builder-skill-low --skill learning-assistant-builder
```

也可以使用完整 GitHub URL：

```bash
npx -y skills add https://github.com/Nagi1998/learning-assistant-builder-skill-low --skill learning-assistant-builder --agent codex
```

### Codex 内置安装器

也可以使用 Codex 自带的 skill-installer：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py --url https://github.com/Nagi1998/learning-assistant-builder-skill-low/tree/main/skills/learning-assistant-builder
```

安装后重启 Codex，让新 skill 生效。

## 其他 Agent 工具复用

如果目标工具不支持 Codex Skill 机制，可以直接复制这个文件内容到其他 Agent 的 System Prompt、Custom Instructions、角色设定或工作流节点中：

```text
skills/learning-assistant-builder/references/portable-agent-prompt.md
```

## Skill 内容

- `skills/learning-assistant-builder/SKILL.md`：Codex Skill 主文件
- `skills/learning-assistant-builder/agents/openai.yaml`：Codex UI 元数据
- `skills/learning-assistant-builder/references/portable-agent-prompt.md`：跨 Agent 通用提示词
