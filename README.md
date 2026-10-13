# Agent Skills

| Skill | 简介 |
| --- | --- |
| [research-decisions](research-decisions/SKILL.md) | 明确科研问题、评估证据与不同解释，选择下一步分析、实验或模拟。 |
| [finish-code-work](finish-code-work/SKILL.md) | 完成范围明确的代码改动，隔离临时测试并清理测试产物。 |
| [notion-project-summary](notion-project-summary/SKILL.md) | 在同一个 Notion 项目页面整理技术成果、协作记录和面试表达。 |
| [presentation-workflow](presentation-workflow/SKILL.md) | 规划、制作和修改演示文稿，统一页面逻辑、排版和验证流程。 |

## 安装

克隆本仓库，将需要的 **整个 skill 目录** 复制到下表对应位置，保持 `<安装目录>/<skill-name>/SKILL.md` 结构。`references/` 等子目录也要一起复制。

```bash
git clone https://github.com/Minato-chen/agent-skills.git
```

| Agent | 全局安装目录 | 项目安装目录 | 官方说明 |
| --- | --- | --- | --- |
| Codex CLI / 本地 Codex | `~/.agents/skills/` | `.agents/skills/` | [Skills](https://developers.openai.com/codex/skills/) |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` | [Skills](https://code.claude.com/docs/en/skills) |
| Cursor | `~/.cursor/skills/` | `.cursor/skills/` | [Skills](https://cursor.com/docs/skills) |
| Gemini CLI | `~/.gemini/skills/` | `.gemini/skills/` | [Skills](https://geminicli.com/docs/cli/skills/) |
| Antigravity IDE / 2.0 | `~/.gemini/config/skills/` | `.agents/skills/` | [Skills](https://antigravity.google/docs/skills) |
| Antigravity CLI | `~/.gemini/antigravity-cli/skills/` | `.agents/skills/` | [Skills](https://antigravity.google/docs/skills) |

`~` 表示用户主目录；Windows 对应 `$HOME`。项目安装目录相对于使用这些 skill 的目标项目。

例如，全局安装到 Antigravity IDE（在克隆的 `agent-skills` 目录内执行）：

**macOS / Linux**

```bash
mkdir -p ~/.gemini/config/skills
cp -R research-decisions finish-code-work notion-project-summary presentation-workflow ~/.gemini/config/skills/
```

**Windows PowerShell**

```powershell
$skillTarget = "$HOME\.gemini\config\skills"
New-Item -ItemType Directory -Force $skillTarget | Out-Null
Copy-Item -Recurse -Force research-decisions, finish-code-work, notion-project-summary, presentation-workflow -Destination $skillTarget
```

其他 agent 将目标目录替换成表中的路径。安装后重新加载 skill 或开启新会话，并在 agent 的 skill 列表中确认；可在提示中明确提及 skill 名称。

ChatGPT Work 的个人 skill 需通过其 Skills 管理入口安装，本地目录安装不会自动同步到账号。Notion skill 需要另行连接 Notion。

更新后重新复制对应目录。旧版 `tau-research-decisions` 已更名为 `research-decisions`；升级时移除安装位置中的旧版目录，避免同时触发。
