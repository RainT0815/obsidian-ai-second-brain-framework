# Lint Prompt

command:: /lint
output:: outputs/health

## 用途

检查这个 vault 是否仍然“有机好用”：有没有孤岛笔记、重复概念、未处理 Inbox、过期项目、模板失效、链接断裂。

## 输入

```text
/lint
请检查当前 vault 的结构健康，并输出一份健康报告。
```

## 检查项

- `01-Inbox` 是否有超过 7 天未处理材料。
- `05-Resources/concepts` 是否存在重复概念。
- `03-Projects` 是否有无下一步行动的项目。
- `02-Daily` 最近 7 天是否连续。
- `04-Areas` 是否有长期无人维护的领域。
- 是否有孤立笔记没有入链或出链。
- `wiki/index.md` 是否和 `wiki/` 实际文件同步。
- `wiki/log.md` 是否记录了最近的 ingest/query/lint。
- `raw/` 中是否有未摄取的重要资料。

## 输出结构

# Vault Health Report - {{date}}

## 总体状态

- 绿 / 黄 / 红：
- 最需要修复的问题：

## 结构问题

-

## 内容问题

-

## 行动建议

- [ ]
- [ ]
- [ ]
