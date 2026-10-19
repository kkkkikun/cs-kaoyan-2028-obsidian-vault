---
type: guide
created: 2026-10-19
tags:
  - github
  - guide
---

# 发布到全新公开 GitHub 仓库

本 Vault 已经包含 README、全部 Markdown 笔记与 Obsidian 配置；**新仓库必须由 GitHub 账号拥有者创建**。以下步骤适用于 Windows 的 PowerShell 或 Git Bash。

## 1. GitHub 建库（约几次点击）

1. 打开 [GitHub New Repository](https://github.com/new)。
2. Repository name：`cs-kaoyan-2028-obsidian-vault`。
3. Visibility：**Public**。
4. 请**不要**勾选 Initialize with README、.gitignore 或 License（压缩包已经有 README 和 .gitignore）。
5. 点击 **Create repository**。

## 2. 下载并解压

下载本 Vault 的 ZIP 并解压；应得到文件夹 `cs-kaoyan-2028-obsidian-vault`，其中能看到 `00-主页.md`、`README.md` 和 `.obsidian` 文件夹。

在文件夹空白处打开 PowerShell / Git Bash；注意命令应在 Vault 根目录运行。**不要**在 ZIP 文件中运行，也不要在文件夹的父目录运行。

## 3. 首次推送（只需一次）

```bash
git init
git branch -M main
git add .
git commit -m "docs: initialize Obsidian study vault"
git remote add origin https://github.com/kkkkikun/cs-kaoyan-2028-obsidian-vault.git
git push -u origin main
```

如果 Git 要求设置作者信息，只为本仓库设置 `git config user.name "..."` 和 `git config user.email "..."`，填写你希望**公开显示在提交记录中的**名字和邮箱（推荐 GitHub 提供的 noreply 邮箱）。不要把访问令牌复制给任何 AI 或写入笔记。

如果使用 Git Credential Manager，Git push 可能打开浏览器要求登录 GitHub；按 Git 官方提示正常授权即可。

## 4. 用 Obsidian 打开

在 Obsidian 选择 **Open folder as vault / 将文件夹作为仓库打开**，选择这份解压后的根目录；打开 `00-主页.md` 即可开始。

之后每次更改如需同步：

```bash
git pull --rebase
git add .
git commit -m "docs: update study notes"
git push
```

如果多设备冲突，先解决冲突，不能直接覆盖。也可以自行安装 Obsidian Git 社区插件，但不是必须。

## 公开仓库隐私提醒

本 Vault 的初始内容只有泛化学习计划与空白模板，不含私人账号信息。以后填写日记、事务收件箱、成绩或附件前，请记住：公开仓库里所有内容可被其他人查看，删除提交也未必消除历史记录。私人事务宜放在独立的私有 Vault。
