# Karpathy Wiki Schema

source:: [[00-Meta/Source/飞书攻略-Karpathy-AI-Obsidian知识库教程]]
version:: v1.2-adapted

## 核心思想

大多数 RAG 系统是在每次提问时重新检索原始资料。Karpathy 式 LLM Wiki 的思路相反：让 AI 逐步维护一个持久、结构化、互相链接的 Markdown wiki。每新增一个来源，AI 不只是索引它，而是把它整合进已有知识网络。

## 三层结构

```text
raw/                  # 原始资料，只读
wiki/                 # AI 维护的知识库
  index.md            # 内容索引
  log.md              # 追加式操作日志
  实体/               # 人、组织、产品、工具
  概念/               # 原理、方法论、术语
  来源/               # 每篇原始资料的摘要
  对比/               # 跨来源横向分析
00-Meta/System/CLAUDE.md
```

## 权限边界

| 层级 | 目录 | 规则 |
|---|---|---|
| 原始资料 | `raw/` | 用户拥有，AI 只读；新增来源时可写入 |
| 编译知识 | `wiki/` | AI 维护，用户阅读和校正 |
| Schema | `00-Meta/System/CLAUDE.md` 与本文件 | 用户和 AI 共同演进 |

## Frontmatter

所有 `wiki/` 页面建议包含：

```yaml
---
type: entity | concept | source | comparison
tags: []
sources: []
created: YYYY-MM-DD
updated: YYYY-MM-DD
---
```

## 页面创建规则

- 每个 raw source 始终创建一个 `wiki/来源/` 摘要页。
- 实体页、概念页、对比页尽量遵守“至少两个不同来源出现后再创建”的规则。
- 第一篇来源出现的概念，先写入来源摘要的 Related Concepts。
- 第二篇来源再次出现同一概念时，再创建独立概念页并回链。

## 工作流

### /ingest

1. 阅读目标 raw source。
2. 创建 `wiki/来源/YYYY-MM-DD 标题.md`。
3. 更新相关实体/概念/对比页。
4. 更新 `wiki/index.md`。
5. 追加 `wiki/log.md`，格式：`## [YYYY-MM-DD] ingest | 标题`。

### /query-wiki

1. 先读 `wiki/index.md`。
2. 再读相关页面和链接。
3. 综合回答并标明来源页面。
4. 若回答值得长期保存，写入 `wiki/对比/` 或对应概念页。
5. 追加 `wiki/log.md`。

### /lint

检查：

- 互相矛盾的说法。
- 孤儿页面。
- 提到但缺页的概念/实体。
- 过时信息。
- `wiki/index.md` 是否与实际文件同步。
- 值得新建的汇总或对比页。

