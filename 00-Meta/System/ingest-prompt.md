# Ingest Prompt

command:: /ingest
schema:: [[karpathy-wiki-schema]]

## 用途

把 `raw/` 里的一个新来源摄取进 `wiki/`，并更新索引和日志。

## 输入

```text
/ingest raw/sources/文件名.md
请按 Karpathy Wiki Schema 摄取这个来源。
```

## 输出步骤

1. 阅读来源。
2. 创建 `wiki/来源/YYYY-MM-DD 标题.md`。
3. 列出 Related Concepts。
4. 判断是否有实体/概念已在至少两个来源出现，需要创建或更新独立页面。
5. 更新 `wiki/index.md`。
6. 追加 `wiki/log.md`。

