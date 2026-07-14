# 编程优秀资源导航

这是一个面向中文开发者与Codex的优质编程仓库索引，集中整理值得学习和参考的开源项目。

> 本仓库只保存项目介绍、机器可读标签和原始链接，不复制第三方源码。项目版权和许可证归原作者所有；使用、修改或分发代码前，请阅读对应仓库的 LICENSE。

## 分类目录

- [计算机基础与学习路线](catalog/learning-roadmaps.md)
- [开发工具与工程资源](catalog/developer-resources.md)
- [AI 与大模型编程](catalog/ai-development.md)
- [PromptCraft与AI桌面程序专项资源](catalog/promptcraft-engineering.md)

## Codex入口

- [AGENTS.md](AGENTS.md)：规定Codex如何选择和使用外部编程知识。
- [repositories.json](data/repositories.json)：按标签、用途和优先级组织的机器可读仓库索引。

当你要求Codex完善程序时，它可以先读取本仓库，再根据任务去上游GitHub仓库查询官方README、文档、源码和测试。例如：

- EXE打包问题 → PyInstaller
- API超时和连接池 → HTTPX
- 重试与限流 → Tenacity
- AI JSON校验 → Pydantic
- 自动化测试 → Pytest
- 多模型路由 → LiteLLM
- 提示词质量评测 → Promptfoo
- 插件协议 → MCP Python SDK

## 收录标准

- 原始仓库真实存在且仍可访问
- 内容具有长期学习或工程参考价值
- 优先选择官方实现、成熟课程、路线图和高质量清单
- 不直接搬运代码，避免版权、更新和安全风险
- 收录不等于安全背书，运行或引入依赖前仍需审查

## 如何使用

1. 根据分类或 `repositories.json` 标签选择相关项目。
2. 让Codex通过GitHub插件读取上游项目的具体文档、实现和测试。
3. 比较不同项目的设计，再决定是否修改当前程序。
4. 确需复用代码时，先检查LICENSE、维护状态、兼容性和安全风险。
5. 只对需要长期修改的项目使用Fork。
6. 依赖优先使用官方包管理器，不要手工复制整个源码。

## 当前规模

目前收录25个优质仓库，覆盖计算机基础、Python工程、桌面UI、Windows打包、文档、网络请求、容灾、测试、多模型、提示词评测、插件协议和系统设计。

## 隐私与安全

禁止向公开仓库提交API Key、Token、客户剧本、用户隐私、生产数据库、未授权Skill或敏感日志。详细规则见 [AGENTS.md](AGENTS.md)。

## 更新原则

新增资源时同时记录：

- 项目名称与原始链接
- 适用任务和查询标签
- 推荐理由与限制
- 许可证检查要求
- 安全与维护状态
