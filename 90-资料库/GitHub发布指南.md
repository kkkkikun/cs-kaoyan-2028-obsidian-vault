---
type: archived-guide
updated: 2026-10-19
tags: [github, obsidian, archive]
---

# GitHub 与 Obsidian 同步说明

> **这份仓库已经创建并发布到 GitHub，原来的“创建新仓库 / git init”步骤不再需要。**
> 请只从 [[00-主页]] 和 [[本周计划]] 开始。此页仅在需要新设备同步时打开。

## 第一次在新电脑上打开

```powershell
git clone https://github.com/kkkkikun/cs-kaoyan-2028-obsidian-vault.git
```

用 Obsidian 打开克隆得到的完整文件夹，查看 `00-日常/00-主页.md`。把 `90-资料库` 折叠，最好将 `本周计划` 加入书签。

## 已经克隆过的电脑

先检查未提交修改，再拉取：

```powershell
git status
git pull --rebase
```

有未提交改动或同一篇笔记在多设备编辑的情况，先保存、提交或处理冲突，**不要强行覆盖**。需要公开备份时先检查差异，只 `git add` 确认可以公开的文件，再 `git commit` / `git push`。

## 当前结构

- `00-日常/`：只有主页、本周计划、毕设一页纸。
- `90-资料库/`：考研/CS/开源等详细资料，以及 `05-模板`、`04-日记`、`06-附件`。
- 原来的笔记内容通过 Git 历史可追溯；深层链接按笔记名称在 Obsidian 中仍可使用。

## 公开仓库提醒

提交前核对隐私。个人日记、准考证、成绩截图、原始照片、私有毕设材料、访问密钥和 Obsidian AI 插件凭据都不应该上传到 Public 仓库。被 `.gitignore` 忽略不等于 AI 插件无法读取，插件的索引范围仍需单独检查。

[[00-主页]] · [[本周计划]] · [[Obsidian使用说明]]
