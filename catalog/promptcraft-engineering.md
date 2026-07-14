# PromptCraft 与AI桌面程序专项工程资源

本页用于指导Codex在优化PromptCraft Director或类似程序时，快速选择最相关的原始仓库。

## Python与桌面程序

### CPython

- 原项目：[python/cpython](https://github.com/python/cpython)
- 适用：线程、并发、标准库、异常、SQLite、Tkinter和Python运行行为。
- 使用方式：遇到语言或标准库边界问题时查询实现和测试，不要把CPython源码复制进业务项目。

### CustomTkinter

- 原项目：[TomSchimansky/CustomTkinter](https://github.com/TomSchimansky/CustomTkinter)
- 适用：现代暗色桌面UI、主题、控件和布局参考。
- 使用方式：先评估迁移成本；现有Tkinter界面稳定时，不应只为视觉效果整体重写。

### PyInstaller

- 原项目：[pyinstaller/pyinstaller](https://github.com/pyinstaller/pyinstaller)
- 适用：Windows单文件EXE、资源打包、隐藏依赖和运行时路径。
- 使用方式：优先参考官方Hooks和Issues，避免用未经验证的打包参数。

### python-docx

- 原项目：[python-openxml/python-docx](https://github.com/python-openxml/python-docx)
- 适用：Word文档生成、段落、表格、样式和分页。
- 使用方式：配合渲染检查，不只验证文件能否打开。

## API稳定性与数据质量

### HTTPX

- 原项目：[encode/httpx](https://github.com/encode/httpx)
- 适用：连接池、超时、同步/异步HTTP和客户端生命周期。
- 适合研究：替换urllib前的性能与迁移评估。

### Tenacity

- 原项目：[jd/tenacity](https://github.com/jd/tenacity)
- 适用：指数退避、Retry-After、停止条件和重试统计。
- 注意：认证、欠费、内容安全等不可恢复错误不应盲目重试。

### Pydantic

- 原项目：[pydantic/pydantic](https://github.com/pydantic/pydantic)
- 适用：AI返回JSON、配置和插件清单的结构化校验。
- 注意：引入前评估EXE体积和现有dataclass迁移成本。

### Pytest

- 原项目：[pytest-dev/pytest](https://github.com/pytest-dev/pytest)
- 适用：并发、失败恢复、插件、导出和性能回归测试。
- 建议：真实API测试与纯本地测试分开，避免日常测试产生费用。

## AI、提示词和多模型

### LiteLLM

- 原项目：[BerriAI/litellm](https://github.com/BerriAI/litellm)
- 适用：多模型统一接口、回退、费用与请求观测。
- 注意：不要为了“支持更多模型”直接引入复杂网关；先明确容灾需求。

### Promptfoo

- 原项目：[promptfoo/promptfoo](https://github.com/promptfoo/promptfoo)
- 适用：提示词对比、模型评测、断言和回归数据集。
- 适合研究：为剧本标准化和Seedance提示词建立质量基准。

### Model Context Protocol Python SDK

- 原项目：[modelcontextprotocol/python-sdk](https://github.com/modelcontextprotocol/python-sdk)
- 适用：工具、资源和插件协议。
- 适合研究：把现有本地插件升级为更标准的扩展接口。

### OpenAI Cookbook

- 原项目：[openai/openai-cookbook](https://github.com/openai/openai-cookbook)
- 适用：结构化输出、工具调用、评测、检索和生产实践。
- 注意：具体API使用应以当前官方文档为准。

### LangChain

- 原项目：[langchain-ai/langchain](https://github.com/langchain-ai/langchain)
- 适用：工作流、工具、模型适配和可观测性架构参考。
- 注意：PromptCraft已有清晰流水线，不应无理由引入大型框架。

### Qwen3

- 原项目：[QwenLM/Qwen3](https://github.com/QwenLM/Qwen3)
- 适用：Qwen模型能力、推理和部署参考。
- 注意：阿里云百炼兼容API的具体参数仍应查询百炼官方文档。

## 推荐研究顺序

1. 先定位当前程序的真实瓶颈。
2. 从本页选择最相关的2到5个仓库。
3. 使用GitHub插件读取具体文档、测试和实现。
4. 形成设计比较，不直接照抄。
5. 小步修改并增加回归测试。
6. 使用真实样本验证速度、质量和失败恢复。
