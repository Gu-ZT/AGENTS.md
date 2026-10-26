<div align="center">

# AGENTS.md

**自用的 AI 编程助手全局规则，让 AI 写代码、提 PR 更守规矩。**

</div>

## 简介

这里维护了一份通用的 `AGENTS.md`，用来约束 AI 编程助手的日常行为。规范采用渐进式披露：入口文件只保留每次任务都适用的强制约束和索引，具体细则按主题放在 `docs/rules/`，AI 按当前任务读取对应文档。

## 管了哪些事

- **怎么说话**：统一回复、文档、注释和 Commit 的文风。
- **怎么干活**：拿不准先问，别留半成品，只改该改的代码，做好异常处理。
- **怎么测试**：修 Bug 先写复现，改完跑局部测试，提交前做好检查。
- **怎么写代码**：命名、拆模块、接口暴露、注释和格式要求。
- **怎么看代码**：规定用什么工具搜代码、搜哪里，以及怎么让子代理帮忙 Review。
- **特定技术栈**：前端、Java 和 Gradle 的专门避坑指南。
- **怎么交代码**：遵循 Conventional Commits，按步骤提交，别夹带无关改动。

规则入口见 [AGENTS.md](AGENTS.md)，按主题拆分后的细则见下方文档结构。

## 文档结构

- [AGENTS.md](AGENTS.md)：规范入口，包含适用范围、每次任务强制约束与专题索引。
- [language-and-style.md](docs/rules/language-and-style.md)：回复、文档、注释与提交信息的文风要求。
- [workflow.md](docs/rules/workflow.md)：需求澄清、完整交付、最小变更、错误处理与测试验证。
- [coding-and-design.md](docs/rules/coding-and-design.md)：命名、抽象、模块划分、注释与代码格式。
- [exploration-and-review.md](docs/rules/exploration-and-review.md)：检索工具、探索范围与子代理审查。
- [frontend.md](docs/rules/frontend.md)：`web/` 前端的包管理、主题颜色、滚动区域与弹出层。
- [java-and-gradle.md](docs/rules/java-and-gradle.md)：Java 代码风格、空安全注解与 Gradle 验证。
- [version-control.md](docs/rules/version-control.md)：提交粒度、提交信息、暂存检查与推送规则。

## 用法

放到项目根目录，或者配到 AI 工具的全局 Prompt 里。优先级：**你的口头指令 > 项目局部规范 > 这份全局规范**。

文件头部的 `trigger: always-on` 表示默认全局加载，不同工具按各自的方式配就行。

## 维护说明

更新条款时别写废话，直接写清楚“要做什么”、“别做什么”以及“为什么（技术后果）”，保持例子和规则一致。规则按主题写入对应专题文档，入口文件只保留全局约束和索引。Commit 格式用 `type(scope): 简短中文摘要`，提交前检查下 diff 和多余空格。

## 许可证

[MIT License](LICENSE)
