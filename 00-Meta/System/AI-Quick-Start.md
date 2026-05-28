# AI 快速上手——给 AI 的指令

> 复制下面这段给你的 AI 助手。它会帮你搭建、配置和运行这个知识库。

## 第一步：搭建 vault（只做一次）

请基于这个 GitHub 仓库帮我搭建一个 Obsidian AI 第二大脑：
https://github.com/RainT0815/obsidian-ai-second-brain-framework

步骤：
1. 克隆这个仓库到本地
2. 帮我填写 00-Meta/Personal/给AI的自我介绍.md（通过提问引导我回答）
3. 告诉我这个 vault 的核心规则和每日流程

## 第二步：每日流程

### 早上：启动一天
请读取 02-Daily/Todo/今天.md 和 02-Daily/Journal/今天.md，帮我确认今天最重要的一件事是什么。然后按上午/中午/下午/晚上排成时间块。

### 阅读/观看后：沉淀知识
我把一篇资料放到了 01-Inbox/。请帮我做 Ingest：
1. 读取资料，提炼要点
2. 在 05-Resources/summary/ 里生成摘要
3. 如果有可复用的概念，存到 05-Resources/concepts/
4. 更新 05-Resources/log.md 记录操作

### 晚上：复盘
请按以下流程帮我做晚间复盘：

第一步：提问复盘
- 今天完成了什么？（工作 + AI 学习）
- 今天偏离了 AI 主线吗？
- 今天输入过载、输出不足了吗？
- 今天的小输出是什么？
- 明天最小下一步是什么？

第二步：建立明日 Todo
- 把明天的任务写入 02-Daily/Todo/明天.md

第三步：沉淀判断
- 今天的内容哪些值得进 05-Resources？

第四步：健康检查
- 偏离主线？输入过载？输出不足？精力透支？

## 第三步：每周回顾（周末用）

请帮我做本周回顾：
1. 读取本周所有 Daily Journal
2. 生成 Weekly Learning Report 写入 02-Daily/Weekly-Learnings/
3. 检查 03-Projects 下每个项目的进度
4. 运行一次 /lint，检查 vault 健康度

## 核心规则（AI 必须遵守）

1. 会话启动优先走主线
2. P0(主线) > P1(知识沉淀) > P2(vault优化)
3. 先提问再操作，不要替用户做决定
4. log.md 必须更新
5. 每天至少确保一个小输出
