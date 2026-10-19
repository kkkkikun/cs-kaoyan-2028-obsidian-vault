---
type: guide
created: 2026-10-19
tags:
  - obsidian
  - guide
---

# Obsidian 使用说明

## 无插件快速入门

1. 解压 Vault 到一个普通文件夹；在 Obsidian 选择「将文件夹作为仓库打开」。
2. 从 [[00-主页]] 开始。双中括号包裹笔记名是内部链接；Ctrl/Cmd+O 可快速查找笔记。
3. 内置 Templates 插件：设置模板目录 `05-模板`，使用 [[日记模板]]、[[周计划模板]] 等。
4. 内置 Daily notes 插件：日记目录 `04-日记`，模板 `05-模板/日记模板`。
5. 不启用 Dataview 也能完整使用。所有任务都是普通 Markdown `- [ ]`，GitHub 也能显示。

## Git 与设备间同步

建议先掌握最简单的 Git 同步：`git pull --rebase`（编辑前）→ Obsidian 编辑 → `git add .` → `git commit` → `git push`。如有冲突，先人工检查，不要自动覆盖本地笔记。

## 公开存储边界

此仓库公开，适合知识笔记和泛化计划；个人每日行程、成绩截图、私人事务、学号/地址、账号或任何令牌，不应提交。尤其不要把带姓名的四级准考证、真实学校信息和私人的每日生活记录放进公开仓库。

注意 Obsidian 不会自动把本 Vault 与 ChatGPT 或 GitHub 同步；要通过 Git 命令或合适的同步插件实现。

[[00-主页]] · [[每日学习记录指南]]
\n
## 配合 AI 插件的实际操作

已安装 AI 插件时，先阅读 [[AI插件工作流]]。不同插件的入口、对笔记的访问范围和是否联网不同：可以选中笔记让它整理，但在未确认插件行为前不要让它自动批量写入。

**注意公开仓库的隐私边界：** `04-日记/` 适合在本地保存个人记录，`.gitignore` 会忽略新的日记文件（保留公开的 README）；带有隐私信息的草稿请保存在独立私有 Vault，或明确不会提交的 `99-私人笔记/` 目录。即便 Git 忽略它们，AI 插件依然可能读取，所以要额外检查 AI 插件的索引/授权范围。

## 仓库现在已经在 GitHub 的最短使用流程

```powershell
git clone https://github.com/kkkkikun/cs-kaoyan-2028-obsidian-vault.git
```

用 Obsidian 将克隆后的根目录打开为 Vault。每天从 [[00-主页]] 和 [[本周计划]] 出发，周末再检查一次 [[开源贡献记录]] 和 [[AI项目停车场]]。

同步时先 `git pull --rebase`，编辑完成后检查 `git status` 和待提交文件，再 `git add` 指定的公开笔记、`git commit` 与 `git push`。**不要在这个公开仓库盲目运行 `git add .`**。
