# Context Loading Prompt

purpose:: 让 AI 在开始工作前读取 vault 的关键上下文
command:: /context

## 目的

在做任何项目和决策之前，先读取这座 vault，生成一份综合性的“我是谁、我在做什么、我最近在关心什么”的总结。

## 执行触发词

- `/context`
- `/scan`
- `/summary`

## 输出结构（五大模块）

### 1. 我是谁（Identity & Vision）

读取：

- `00-Meta/Personal/`
- `00-Meta/System/`
- `04-Areas/`
- `02-Daily/Journal/`

输出：

- 核心身份
- 长期目标
- 当前价值观
- 最近的身份变化

### 2. 我现在在做什么（Active Projects）

读取：

- `03-Projects/`
- 最近 14 天的 daily notes

输出：

- 正在推进的项目
- 每个项目的目标、下一步、阻塞点
- 需要我今天处理的事项

### 3. 我最近在想什么（Recent Thinking）

读取：

- `02-Daily/Weekly-Learnings/`
- `05-Resources/summary/`
- `05-Resources/concepts/`

输出：

- 最近反复出现的主题
- 新出现的观点或认知变化
- 值得继续研究的问题

### 4. 未解决的问题与假设（Open Issues）

输出：

- 未解决问题
- 决策缺口
- 缺失资料
- 可以验证的假设

### 5. 下一步建议（Next Actions）

输出：

- 3 个今天可执行动作
- 1 个本周重点
- 1 个应该归档或放弃的事项

