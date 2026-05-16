# 贡献指南

感谢你愿意一起完善这份 AI 快速学习手册。

## 可以贡献什么

- 修正概念错误或不严谨表述
- 补充官方文档来源
- 新增 AI 热词、模型、Agent 工具、框架和方法论
- 补充真实案例
- 改进 HTML 页面结构、交互和移动端体验
- 把内容整理成适合飞书文档、小红书图文或课程讲义的版本

## 内容原则

1. 先通俗，再专业  
   先用普通人能懂的话解释，再补充必要技术细节。

2. 优先官方来源  
   涉及模型、工具、框架和协议时，优先引用官方文档、项目仓库或论文。

3. 区分事实和观察  
   对 OpenClaw、Hermes 等快速变化或同名项目较多的工具，要标注“需核验具体项目来源”。

4. 不夸大能力  
   不把演示效果写成稳定能力，不把 Agent 写成万能自动化。

5. 保留风险边界  
   每个词条都应该说明限制、误区或落地风险。

## 词条格式

词条数据位于：

```text
docs/ai-manual-data.js
```

新增词条建议包含：

```js
{
  id: 71,
  title: "词条名称",
  tag: "分类",
  summary: "一句话解释。",
  use: "典型使用场景。",
  risk: "限制、误区或风险。"
}
```

请确保：

- `id` 不重复
- `tag` 尽量复用已有分类
- 表达自然、简洁
- 不写未经核实的绝对化判断

## Pull Request 建议

提交 PR 时请说明：

- 改了哪些内容
- 为什么要改
- 是否补充了来源
- 是否检查了页面是否能正常打开

## 本地检查

可以用下面命令检查词条数据是否能被正常加载：

```bash
node - <<'NODE'
const fs = require('fs');
const vm = require('vm');
const data = fs.readFileSync('docs/ai-manual-data.js', 'utf8');
const context = { window: {} };
vm.createContext(context);
vm.runInContext(data, context);
const terms = context.window.AI_MANUAL_TERMS;
const ids = terms.map((term) => term.id);
const duplicateIds = ids.filter((id, index) => ids.indexOf(id) !== index);
console.log({ count: terms.length, duplicateIds });
NODE
```

也可以直接打开：

```bash
open docs/ai-manual-prototype.html
```
