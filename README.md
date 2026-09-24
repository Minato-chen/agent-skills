# Agent Skills

两个可复用的 Agent Skill。每个目录中的 `SKILL.md` 是独立入口；安装时复制**整个 Skill 目录**，让文件保持 `<skill-name>/SKILL.md` 的结构。

| Skill | 用途 |
| --- | --- |
| [`tau-research-decisions`](tau-research-decisions/SKILL.md) | 为 Tau K18 电荷排列与相分离研究挑选最小、可区分不同解释的下一步分析；区分观测、解释与未知。 |
| [`finish-code-work`](finish-code-work/SKILL.md) | 约束代码改动、验证、开源协作及里程碑收尾；在同一个 Notion 项目页面整理技术记录、协作和面试表达。 |

Skill 是工作指令，不会自行提供 GitHub、Notion 或 Godot 的访问权限。需要相应应用的连接和授权。`finish-code-work` 在 Notion 无法访问时会准备可粘贴内容，并说明未保存。

## Antigravity IDE：macOS / Windows

先克隆仓库，再把两个目录复制到全局 Skill 位置。这样所有项目都可以使用。

**macOS（终端）**

```bash
git clone https://github.com/Minato-chen/agent-skills.git
mkdir -p ~/.gemini/config/skills
cp -R agent-skills/tau-research-decisions agent-skills/finish-code-work ~/.gemini/config/skills/
```

**Windows（PowerShell）**

```powershell
git clone https://github.com/Minato-chen/agent-skills.git
New-Item -ItemType Directory -Force "$HOME\.gemini\config\skills" | Out-Null
Copy-Item -Recurse -Force .\agent-skills\tau-research-decisions, .\agent-skills\finish-code-work "$HOME\.gemini\config\skills\"
```

如果已经在名为 `agent-skills` 的目录内执行命令，把源路径开头的 `agent-skills/`（PowerShell 为 `.\agent-skills\`）去掉。也可以只用于某个项目：将两个目录放进该项目的 `.agents/skills/`。在 Antigravity IDE 的 Agent 侧栏 **Customizations** 检查识别结果；在提示中提及 Skill 名称可明确调用。全局 IDE 路径是 `~/.gemini/config/skills/`，Antigravity CLI 的全局目录则是 `~/.gemini/antigravity-cli/skills/`；两者都支持项目级 `.agents/skills/`。

### Antigravity IDE：Notion 和 Godot MCP

Agent 侧栏 `… → MCP Servers → Manage MCP Servers → View raw config` 可打开全局 `~/.gemini/config/mcp_config.json`。已有配置时，**合并**下列两项到现有的 `mcpServers`，不要覆盖其他服务：

```json
{
  "mcpServers": {
    "notion": {
      "serverUrl": "https://mcp.notion.com/mcp"
    },
    "godot": {
      "command": "npx",
      "args": ["-y", "@coding-solo/godot-mcp"]
    }
  }
}
```

Notion 是官方远程 MCP；在 Antigravity 的 **Customizations** 中对该服务执行 **Authenticate**，在浏览器完成 OAuth 授权。Godot MCP 是 Coding-Solo 的本地服务，需要 Godot、Node.js 18+ 和 npm。如果找不到 Godot，在 `godot` 条目加入 `"env": {"GODOT_PATH": "Godot 可执行文件的绝对路径"}`。macOS 可用应用内可执行文件路径，Windows 可用 `C:\\...\\Godot_v4.x.exe`（JSON 反斜线需双写）。如果找不到 `npx`，把 `command` 改为本机 `npx`/`npx.cmd` 的绝对路径。不要把个人路径、OAuth 令牌或私密配置提交到本仓库。

MCP 配置和授权要在每台电脑分别完成。安装后刷新 MCP 服务列表，分别测试读取一个有权限的 Notion 页面和查询 Godot 版本；在实际项目操作前确认项目目录中有 `project.godot`。

## ChatGPT Work / Codex

ChatGPT Work 的个人 Skill 需要在它自己的 Skills 目录中安装；仅克隆 GitHub 仓库不会自动同步到 ChatGPT。目前 `finish-code-work` 已单独安装在该账号的 ChatGPT Work 中。需要使用 GitHub 版本时，在 Skills 界面导入相应 Skill 文件夹，或按当前产品的个人 Skill 安装流程操作。

对于本地 Codex 工作流，可以在任务中明确提供 `SKILL.md` 路径，并按所用 Codex 版本的 Skill 安装说明放到其个人 Skill 目录。项目专属约定写在该项目的 `AGENTS.md`；这些通用 Skill 不包含某个仓库的测试命令或数据路径。

## 更新

修改后检查 YAML frontmatter 的 `name`、`description` 和实际行为，再将更新推到此仓库。复制安装的版本不会自动更新；重新复制对应目录。Notion 页面和 MCP 登录状态不属于仓库内容。

## 参考

- [Google Antigravity Agent Skills](https://antigravity.google/docs/skills)
- [Google Antigravity MCP](https://antigravity.google/docs/mcp)
- [Notion MCP](https://developers.notion.com/guides/mcp/get-started-with-mcp)
- [Coding-Solo Godot MCP](https://github.com/Coding-Solo/godot-mcp)
