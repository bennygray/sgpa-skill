# SGPA — Senior Game Product Analyst Skill

> 资深游戏产品制作人 & 系统架构师分析框架 v1.0

## 简介

SGPA 是一个面向 AI 编码助手的 **Skill**（技能扩展），用于指导大型游戏系统的全生命周期需求分析。
覆盖 MECE 需求分析、架构拆解、User Story 生成、执行指导、数值验证和交付交接。

## 核心理念

当 AI 助手承接大型系统需求（如 AI 灵智系统、道侣系统、经济体系重设计）时，
**绝不立即陷入代码细节**，必须严格通过 **四个阶段、十个步骤** 进行正交分解。

## 四阶段十步骤

```
Phase I  需求分析 ─── Step 1 价值锚定 → Step 2 实体数据 → Step 3 规则数值
                      ↓ (Self-Review + USER 确认)
Phase II 架构拆解 ─── Step 4 架构分层 → Step 5 分期路线图 → Step 6 User Story
                      ↓ (Self-Review + USER 确认)
Phase III 执行指导 ── Step 7 文档先行 → Step 8 验证脚本指引
                      ↓ (编码完成)
Phase IV 验证交付 ─── Step 9 集成验证 → Step 10 交接归档
```

## 文件结构

```
sgpa-skill/
├── SKILL.md                              ← 核心指令（AI 助手阅读此文件）
├── references/
│   ├── anti-patterns.md                  ← 反模式清单
│   ├── progress-template.md              ← 分析进度模板
│   ├── user-story-template.md            ← User Story 标准模板
│   └── verification-checklist-template.md ← 验证清单模板
├── examples/                             ← 使用示例（待补充）
├── README.md
└── LICENSE
```

## 使用方法

1. 将本仓库内容复制到项目的 `.agents/skills/product-manager/` 目录下
2. 在项目的 AGENTS.md 或 AI 助手环境中引用此 Skill
3. 当提出大型系统需求时，AI 助手将自动触发 SGPA 流程

## 适用场景

- 新子系统设计（如弟子系统、装备系统、经济体系）
- 重大功能重构
- 跨系统架构审计
- 数值体系重设计

## 设计原则

| 原则 | 说明 |
|------|------|
| **HARD-GATE** | Phase 间严格门禁，每个 Phase 必须 USER 确认后才能进入下一阶段 |
| **MECE** | 所有分析结果必须相互独立、完全穷尽 |
| **数值先行** | 涉及数值的设计必须输出可程序验证的公式 |
| **文档先行** | 先更新文档 → USER 确认 → 编码 |
| **反合理化** | 内置 AI 自检机制，防止跳步或过度设计 |

## 版本历史

| 版本 | 日期 | 变更 |
|------|------|------|
| v1.0 | 2026-03-27 | 首次发布。四阶段十步骤完整框架。 |

## License

MIT
