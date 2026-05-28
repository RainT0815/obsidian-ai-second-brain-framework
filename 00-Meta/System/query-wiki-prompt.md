# Query Wiki Prompt

command:: /query-wiki
schema:: [[karpathy-wiki-schema]]

## 用途

基于 `wiki/` 中已经编译的知识回答问题，而不是直接从零读所有 raw sources。

## 输入

```text
/query-wiki
问题：...
如果回答有长期价值，请保存为 wiki 页面。
```

## 输出要求

- 先读取 `wiki/index.md`。
- 标明使用了哪些 wiki 页面。
- 回答中使用 Obsidian 双链。
- 如果形成新综合，保存到 `wiki/对比/` 或相关概念页。
- 追加 `wiki/log.md`。

