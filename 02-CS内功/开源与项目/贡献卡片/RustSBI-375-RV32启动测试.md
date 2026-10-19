---
type: contribution-candidate
status: candidate
checked: 2026-10-19
tags: [opensource, rustsbi, riscv, os]
---

# RustSBI #375｜RV32 最小 Linux 启动测试

- 主 Issue：[RustSBI CI #307](https://github.com/rustsbi/rustsbi/issues/307)
- 任务 Issue：[RustSBI #375](https://github.com/rustsbi/rustsbi/issues/375)
- 核查状态（2026-10-19）：**Open；无已显示认领者 / 评论**。这是机会，不是自己已经合并或提交的成果。
- 目标：在 `qemu-system-riscv32` 上通过 RustSBI Prototyper 验证 Linux 进入 userspace。
- 上游列出的路径：RustSBI → Linux → userspace（Bare SBI）；RustSBI → U-Boot(S-mode) → Linux → userspace。

## 先做最小闭环（未完成，不能打勾）

- [ ] 核对 Issue、PR、分支是否已经有人实现同一范围。
- [ ] 阅读已有 RV64 CI / 启动脚本，识别可复用部分。
- [ ] 在可用环境里确认 QEMU RV32 与内核、固件的版本及来源。
- [ ] **优先 Bare SBI**：实际运行并保存序列控制台输出，确认 userspace。
- [ ] 再评估 U-Boot 路径；无法验证时明确记录原因。
- [ ] 只有在有可重复证据后，考虑最小化补丁、文档和 PR。

## 证据区

- 命令 / 版本：
- 环境：
- 实际日志（仅公开、安全、脱敏内容）：
- 成功 / 失败：
- 下一个最小任务：

## 学习价值

RISC-V SBI、特权级、引导链、QEMU、操作系统启动与 CI，能与 [[OS训练营学习路线]] 和 [[408-操作系统]] 串联。

> 本页只记录路线，不声称实验已经通过。四级前建议最多投入少量定向调研，不挤占数学和英语。

[[开源贡献记录]] · [[AI项目停车场]]
