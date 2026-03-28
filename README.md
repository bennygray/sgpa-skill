# Trinity Pipeline — Multi-Agent Game Development Skills

> **Version**: v2.0 | **License**: MIT
> **Evolution**: SGPA (v1.0 单体) → Trinity (v2.0 三角分工)

## Overview

Trinity Pipeline 是一个多智能体游戏开发技能框架，将产品分析、架构设计和编码实施分为三个独立的 Agent Skill，通过 Gate 签章机制串联。

## 架构

```
USER 需求 → /SPM (Gate 1) → /SGA (Gate 2) → /SGE (Gate 3) → 交付
              What/Why         Where/How        Build/Verify
```

## 三个 Skill

| Skill | 角色 | 职责 | Gate |
|-------|------|------|------|
| `/SPM` | Senior Product Manager | 需求分析、价值锚定、User Story | Gate 1 |
| `/SGA` | Senior Game Architect | Interface 设计、Pipeline 挂载、ADR | Gate 2 |
| `/SGE` | Senior Game Engineer | 编码实施、数值验证、回归测试 | Gate 3 |

## 共享模块 (`_shared/`)

| 模块 | 用途 |
|------|------|
| `review-protocol.md` | Party Review 三层防线（L1 穷举 → L2 CoVe → L3 辩论） |
| `cove-protocol.md` | Chain of Verification Evidence 证据验证 |
| `communication-rules.md` | 沟通纪律（禁止自说自话） |
| `anti-rationalization.md` | 反合理化清单 |
| `change-management.md` | 变更管理协议 |
| `personas/` | Review 角色定义（7 个角色） |
| `templates/` | ADR / Pre-Mortem / Assumption Audit 模板 |

## 特性

- **Gate 签章机制**: 上游未签章 → 下游拒绝执行
- **Party Review**: 多角色对抗审查（魔鬼PM、偏执架构师、找茬QA 等）
- **CoVe 证据验证**: 对 WARN/BLOCK 项执行独立证据验证
- **技术/需求债务追踪**: 与 `tech-debt.md` / `feature-backlog.md` 集成
- **第一性原理**: SPM 阶段强制 5-Why 分析
- **反合理化**: 每个 Skill 有专属的反合理化清单

## 从 SGPA v1.0 升级

SGPA v1.0 是单体 10 步分析框架。Trinity v2.0 将其拆分为三个独立 Skill：

| SGPA v1.0 | Trinity v2.0 |
|-----------|-------------|
| Step 1-4 (分析/锚定/规则/Story) | `/SPM` |
| Step 5-7 (架构/Interface/Pipeline) | `/SGA` |
| Step 8-10 (编码/验证/回归) | `/SGE` |

## 安装

将本仓库内容复制到项目的 `.agents/skills/` 目录下即可。

## 版本历史

| 版本 | 日期 | 变更 |
|------|------|------|
| v2.0 | 2026-03-28 | Trinity Pipeline：SPM + SGA + SGE 三角分工 + 债务文档集成 |
| v1.0 | 2026-03-27 | SGPA 单体：10 步分析框架 |
