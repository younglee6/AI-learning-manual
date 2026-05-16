# AI 快速学习手册

一份面向非技术同学、个人学习者和 AI Coding 入门者的 AI 学习手册。

它不是技术百科，而是一张可以持续维护的学习地图：用通俗语言解释 AI 热词、大模型、Prompt、RAG、Agent、MCP、Skill、AI Coding 与 Agentic Engineering，并把相关词条之间的关系可视化出来。

## 在线阅读

本项目当前主页面是：

- [AI 快速学习手册 HTML 原型](./docs/ai-manual-prototype.html)

如果开启 GitHub Pages，可以选择从仓库根目录发布，访问 `index.html`；也可以选择从 `docs/` 目录发布，访问 `docs/index.html`。

## 适合谁

- 想快速理解 AI 常见热词的人
- 经常听到 RAG、Agent、MCP、AI Coding，但还没形成完整知识框架的人
- 想把 AI 学习内容整理成飞书文档、网页或知识库的人
- 想向团队、朋友或小红书读者分享 AI 入门内容的人

## 内容结构

- 文档简介：说明这份手册讲什么、依据什么、怎么读、怎么更新
- 核心词条：70 个词条，支持搜索、标签筛选和点击查看详情
- 关系图：展示词条从基础认知到工程落地的结构关系
- 核心模块：按“是什么 / 能力 / 场景 / 限制 / 方法 / 案例”展开
- 小红书卡片版：适合做图文分享的内容草稿

## 当前核心模块

- AI 基础认知
- 大模型 LLM
- 模型与产品生态
- Prompt 工程
- 上下文管理
- RAG
- 知识库
- Agent
- Agent 工具生态
- 工具调用
- MCP
- Skill
- Agent Harness
- AI Coding 工作流
- Agentic Engineering

## 内容依据

手册优先参考官方文档和主流项目文档，包括但不限于：

- OpenAI API / Codex / Agents SDK
- Anthropic Claude / Claude Code
- Google Gemini
- Model Context Protocol
- LangGraph / AutoGen / LlamaIndex 等项目文档

AI 生态变化很快。涉及具体产品、模型、Agent 工具和开源项目时，请以官方文档、项目仓库和最新发布信息为准。

## 本地使用

这个项目不需要安装依赖，可以直接打开 HTML 文件：

```bash
open docs/ai-manual-prototype.html
```

也可以用任意静态服务器预览：

```bash
python3 -m http.server 8000
```

然后访问：

```text
http://localhost:8000/docs/ai-manual-prototype.html
```

## 如何更新词条

词条数据在：

```text
docs/ai-manual-data.js
```

每个词条包含：

- `title`：词条名称
- `tag`：分类标签
- `summary`：一句话解释
- `use`：使用场景
- `risk`：注意事项或误区

建议新增词条时同时补充：

- 官方来源链接
- 容易混淆的概念
- 真实应用场景
- 是否属于快速变化的生态工具

## 贡献方式

欢迎通过 Issue 或 Pull Request 贡献：

- 修正不准确的词条解释
- 补充官方引用
- 新增 AI 热词
- 优化模块内容
- 增加案例
- 改进页面交互和移动端体验

提交前请阅读 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## 许可协议

本项目采用双许可：

- 代码部分：MIT License，见 [LICENSE](./LICENSE)
- 文档内容：Creative Commons Attribution 4.0 International，见 [CONTENT-LICENSE.md](./CONTENT-LICENSE.md)

你可以学习、转载、改编和二次创作。引用或分享时请保留来源说明。

## 免责声明

这份手册是学习资料，不构成技术选型、法律、合规、安全或投资建议。AI 产品、模型能力和工具生态更新很快，正式使用前请回到官方文档核验。
