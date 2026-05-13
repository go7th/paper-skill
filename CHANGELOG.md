# Changelog

本项目遵循 [Semantic Versioning](https://semver.org/lang/zh-CN/)。

## [0.2.0] - 2026-05-13

### 重构
- SKILL.md 拆分为路由文件 + 分层子文件（Progressive Disclosure），减少每次激活的 token 占用
- 6 级表格顺序调整为 S → A → B → SS → C → D，避免新读者误把 SS 当默认
- S 级 6 专家 prompt 替换过时的 jailbreak 写法（"请你忘记你是协助我的 AI"），改用标准 role-play
- 文档术语统一为"方案"

### 新增
- 方案类型识别：根据方案类型（技术 / 产品 / 业务 / 设计）自动切换专家组
- S 级循环硬上限：最多 3 轮，避免无限挑刺
- 输入 / 输出规范章节：明确文件路径接入、输出新文件副本、不改原文件
- 执行完成 checklist：跑完输出 markdown 清单让用户验证
- 触发词英文版 + 反触发词机制：用户明确说"不要藏话"时强制禁用 C/D
- `tiers/` 目录：s-tier / ss-tier / cd-tier / a-b-tier 详细规则
- `prompts/expert-critique.md`：分方案类型的专家 prompt 模板
- CHANGELOG.md

### 修复
- H1 标题从 "Bulletproof Proposal" 改为 "paper-skill"，与 frontmatter `name` 一致
- C 级触发词 `白字` → `白字白底` / `白色文字隐藏`，避免误命中"白字红底警告标"等正常表述

## [0.1.0] - 2026-05-13

### 首版
- 6 级策略分级（S / A / B / SS / C / D）
- 默认 S + A 组合
- SS / C / D 显式触发 + 强制警告机制
- 5 个必备防御章节模板
- 章节命名禁用词清单
- MIT License
