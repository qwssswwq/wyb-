# Codex Knowledge Routing Guide

本仓库是编程知识导航库，不是第三方源码镜像。

## Codex在本仓库中的默认工作方式

当用户要求设计、诊断、优化或重构程序时：

1. 先阅读 `README.md`、相关 `catalog/*.md` 和 `data/repositories.json`。
2. 根据任务标签选择2到5个最相关的上游仓库。
3. 使用GitHub插件按需读取上游仓库的官方README、文档、源码、测试和最近变更。
4. 优先引用官方项目、原始仓库和官方文档，不依赖二次转载。
5. 先总结可借鉴的架构与权衡，再决定是否修改当前程序。
6. 不批量复制第三方源码；确需复用时，先检查LICENSE、版本兼容性和安全风险。
7. 不因为某项目流行就直接引入依赖；优先解决当前项目的具体问题。
8. 任何外部仓库写入、Fork、Issue、PR或发布动作都必须得到用户明确授权。

## PromptCraft类项目的路由规则

- Python运行时与语言行为：`python/cpython`
- Windows EXE打包：`pyinstaller/pyinstaller`
- 桌面UI设计：`TomSchimansky/CustomTkinter`
- Word文档：`python-openxml/python-docx`
- HTTP客户端与超时：`encode/httpx`
- 重试与退避：`jd/tenacity`
- 结构化校验：`pydantic/pydantic`
- 自动化测试：`pytest-dev/pytest`
- 多模型路由：`BerriAI/litellm`
- 提示词与模型评测：`promptfoo/promptfoo`
- 插件与工具协议：`modelcontextprotocol/python-sdk`
- 大模型应用范式：`openai/openai-cookbook`
- Qwen模型参考：`QwenLM/Qwen3`
- 系统设计：`donnemartin/system-design-primer`

## 安全边界

禁止把以下内容写入公开仓库：

- API Key、Token、密码或云服务凭据
- 客户剧本、用户隐私和生产数据库
- 未获授权的提示词Skill或第三方付费资料
- 本地绝对路径、聊天记录或敏感日志
- 可被滥用的真实密钥诊断响应

提交代码前应检查 `.gitignore`、配置文件、测试样本和导出目录。

## 研究输出要求

每次借鉴外部项目时，应说明：

- 查询了哪些原始仓库
- 借鉴了什么设计
- 为什么适合当前程序
- 没有采用哪些部分及原因
- 是否新增依赖
- 许可证与安全影响
- 测试和验证结果
