你这个反馈是对的。上一版的问题是：我给的是“**软件工程词汇分类表**”，但你真正需要的是“**软件工程师脑中的概念模型**”。

也就是说，你不是想知道：

> ownership = 责任

而是想知道：

> 为什么工程师遇到这种情况会想到 ownership，而不是 responsibility？
> 这个词背后对应什么工程文化？
> 和其他相近词有什么边界？

下面我重新整理。会保持之前那种方式：**概念来源 → 使用场景 → 对比 → 常见表达**。

---

# 1. Ownership：工程里的“责任归属模型”

这是软件工程文化里最核心的词之一。

## 背后的思想

工程团队默认一个原则：

> Every important thing should have a clear owner.

任何重要东西，都应该有人负责。

这个“东西”可以是：

- 一个服务
- 一个代码模块
- 一个 Bug
- 一个文档
- 一个技术方案
- 一个客户问题

---

## Owner ≠ Responsible person

很多中文使用者会翻：

> 负责人 = responsible person

但是工程团队不是这样理解的。

### Responsible

强调：

> 这个人在职责范围内负责某件事。

例如：

> The backend team is responsible for the API service.

意思：

后端团队负责 API 服务这个领域。

---

### Owner

强调：

> 如果出了问题，谁需要推动事情最终落地？

例如：

> Who owns this incident?

意思：

谁负责推动这个事故处理完成？

可能：

- 找人
- 协调
- 更新状态
- 推动修复

---

## Assignee 和 Owner 的区别

这是 Jira / GitHub 文化里面非常重要的区别。

假设：

一个支付服务出了 Bug。

结构可能：

```
Payment Service

Owner:
Payment Team

Issue #123

Assignee:
Alice
```

意思：

- Payment Team 对这个服务长期负责
- Alice 当前负责修这个具体问题

所以：

| 词          | 关注点       |
| ----------- | ------------ |
| Owner       | 最终责任归属 |
| Assignee    | 当前执行人   |
| Responsible | 职责范围     |

常见表达：

> The issue doesn't have an owner yet.

（这个问题还没有负责人）

> Let's assign an owner before moving forward.

（继续之前先确定负责人）

---

# 2. Visibility：为什么不用 Transparency？

中文：

> 信息透明

很多人想到：

transparent。

但是工程领域有区别。

---

## Visibility 的核心问题

Visibility 问：

> Can I see what is happening?

关注：

- 状态
- 进度
- 系统行为

例如：

Ticket：

```
Created
 ↓
Assigned
 ↓
In Progress
 ↓
Resolved
```

用户希望：

> I want visibility into the progress.

意思：

我想知道现在处理到哪。

---

## Transparency 的范围更大

Transparency 更多用于：

组织行为：

- decision making
- pricing
- communication

例如：

> The company needs more transparency in decision making.

公司决策过程需要更加透明。

---

## 工程场景：

❌

> We need more status transparency.

虽然能懂，但是不像工程师说话。

✅

> We need better visibility into request status.

---

# 3. Traceability：为什么不是 Tracking？

中文：

> 可追踪

英文有两个容易混：

- tracking
- traceability

---

# Tracking

关注：

> 当前在哪里？

类似快递：

```
Package shipped
      ↓
In transit
      ↓
Delivered
```

软件：

> Track deployment progress.

跟踪发布进度。

---

# Traceability

关注：

> 能不能找到历史关系？

例如：

一个 Bug：

```
Bug
 ↓
Commit
 ↓
Pull Request
 ↓
Code Change
 ↓
Requirement
```

你能不能追溯？

所以：

> Requirement traceability

需求追踪关系。

> Poor traceability

历史关系不清楚。

---

工程里：

Ticket 系统：

需要 tracking。

大型系统：

需要 traceability。

---

# 4. Capture：为什么“沉淀”不用 Accumulate？

这是中文工程文化和英文工程文化差异最大的地方。

中文：

> 经验沉淀下来。

容易想到：

> accumulate knowledge

但是英文工程师不会这么说。

---

## Accumulate

强调数量增加。

例如：

> Data accumulates over time.

数据越来越多。

没有“整理成资产”的意思。

---

## Capture

核心：

> 把原本容易丢失的信息抓取下来。

例如：

会议：

> Capture meeting notes.

记录会议重点。

经验：

> Capture lessons learned.

沉淀经验。

故障：

> Capture troubleshooting steps.

记录排查过程。

---

工程文化：

不是“积累”。

而是：

```
Experience
     ↓
Capture
     ↓
Documentation
     ↓
Reuse
```

---

# 5. Resolve：为什么 Bug 不总用 Fix？

中文：

解决问题。

英文：

fix / solve / resolve 都可以。

但是工程里面有层次。

---

## Fix

修复具体错误。

例如：

> Fix the login bug.

关注：

代码变化。

---

## Resolve

完成问题闭环。

包括：

- 修复
- 验证
- 通知
- 关闭

例如：

> Resolve the incident.

---

## Solve

更偏数学或者复杂问题。

例如：

> Solve a performance problem.

工程管理里：

issue/ticket:

优先：

> resolve

---

# 6. Incident / Problem / Bug：为什么都叫“问题”但英文拆开？

工程文化喜欢分类。

---

## Bug

代码错误。

```
Wrong behavior
↓
Code change needed
```

例：

> The login button doesn't work.

---

## Incident

影响用户或生产环境。

```
System impact
↓
Response needed
```

例：

> Production outage is an incident.

---

## Problem

背后的根因。

```
Incident
   ↓
Why?
   ↓
Problem
```

例如：

Incident：

> API returned 500 errors.

Problem：

> Database connection pool is exhausted.

---

# 7. Standardize vs Centralize：中文都是“统一”

中文：

> 统一流程。

英文至少两个概念。

---

## Centralize

集中。

以前：

```
Email
Slack
Excel
Personal docs
```

之后：

```
Ticket System
```

叫：

> Centralize support requests.

---

## Standardize

规则一致。

例如：

所有服务：

```
same logging format
same deployment process
same API convention
```

叫：

> Standardize the workflow.

---

区别：

|          | Centralize | Standardize |
| -------- | ---------- | ----------- |
| 解决什么 | 分散       | 混乱        |
| 目标     | 一个地方   | 一种规则    |

---

# 8. Dependency vs Blocker：为什么不能都叫阻塞？

---

## Dependency

存在依赖。

A 需要 B。

例如：

Backend:

```
wait for database migration
```

这是：

> dependency

---

## Blocker

导致无法继续。

例如：

> Missing credentials are blocking deployment.

---

关系：

```
Dependency
    ↓
可能导致
    ↓
Blocker
```

依赖不一定阻塞。

---

# 9. Trade-off：为什么架构讨论天天出现？

这是工程文化核心词。

中文：

> 权衡。

但是工程师不是说：

> We need to consider advantages and disadvantages.

太长。

直接：

> There is a trade-off.

例如：

缓存：

优点：

- faster response

缺点：

- stale data

所以：

> We need to consider the trade-off between performance and consistency.

---

# 10. Impact：为什么不用 Effect？

中文：

影响。

---

## Effect

结果。

例如：

> The change had an unexpected effect.

---

## Impact

工程决策影响。

包含：

- 用户
- 成本
- 性能
- 风险

例如：

> What is the impact of this change?

设计评审非常常见。

---

# 11. Maintain vs Operate

中文：

维护。

---

## Maintain

保持状态。

例如：

> Maintain the codebase.

---

## Operate

运行系统。

例如：

> Operate production infrastructure.

区别：

开发：

maintain code

运维：

operate system

---

# 12. Improve vs Optimize

中文：

优化。

---

## Improve

泛提升。

> Improve reliability.

---

## Optimize

针对已有系统做局部最佳化。

例如：

> Optimize database query performance.

通常：

算法、性能、资源：

optimize。

流程、体验：

improve。

---

# 13. Reduce / Prevent / Mitigate

中文：

降低风险。

三个层次。

---

## Prevent

避免发生。

> Prevent failures.

---

## Reduce

降低数量。

> Reduce latency.

---

## Mitigate

已经发生，降低影响。

例如：

服务挂了：

临时方案：

> Apply mitigation.

---

# 14. Software 工程师真正脑中的词汇关系图

不是：

```
中文
 ↓
英文
```

而是：

```
Problem
 |
 +-- Ownership
 |
 +-- Tracking
 |
 +-- Visibility
 |
 +-- Resolution
 |
 +-- Documentation
 |
 +-- Prevention
```

例如一个线上问题：

工程师脑子：

```
Incident happened

Who owns it?

What is the impact?

Can we reproduce?

What's the root cause?

What's the mitigation?

How do we prevent recurrence?

How do we capture the knowledge?
```

这就是工程文化。

---

所以回到你的问题：

> 一般技术开发沟通中也是使用这一套工程文化词汇吗？

答案：

**是，而且这些词不是“正式文档专用”，日常技术沟通也大量使用。**

比如 Slack：

普通人：

> 这个 bug 谁处理？

工程师：

> Who owns this issue?

普通人：

> 现在什么进度？

工程师：

> Any update? What's the current status?

普通人：

> 这个问题怎么避免以后再发生？

工程师：

> How do we prevent this from happening again?

所以你真正需要积累的不是“高级词汇”，而是这些**工程世界里的默认思考模型**。

如果继续深入，下一批最值得学的是：

1. **架构设计词汇（abstraction / coupling / cohesion / scalability）**
2. **代码 Review 文化词汇（nit / LGTM / refactor / technical debt）**
3. **运维事故文化词汇（incident / RCA / mitigation / postmortem）**

## 这些是欧美、日本大型软件团队每天真实使用的语言。

明白你的意思了。你要的不是“软件英语词典”，而是类似一个**软件工程师的语言模型地图**：

- 一个中文概念为什么对应某个英文词；
- 英语工程师为什么选择这个词；
- 它和相近词的边界在哪里；
- 在真实开发沟通里什么时候出现。

这个量比较大，一次消息塞完整会超过合理长度。所以我会拆成几个部分发，保持之前的深度。

这次先给你 **Part 1：工程协作与问题管理（Engineering Workflow & Collaboration）**。
后续继续：

- Part 2：架构设计与代码质量（Architecture & Code Quality）
- Part 3：研发流程与交付（Development Lifecycle & Delivery）
- Part 4：运维、稳定性、事故管理（SRE / Production）
- Part 5：项目管理与技术沟通（Engineering Communication）
- Part 6：开源、社区、Git 文化（Open Source Culture）

---

# Part 1：Engineering Workflow & Collaboration

---

# 1. Ownership（责任归属）

## 核心思想

软件工程文化里面有一个默认假设：

> If nobody owns it, it won't get done.

如果没有明确负责人，事情很容易消失。

所以工程团队非常重视：

- owner
- ownership

---

## Owner

不是“拥有者”。

而是：

> The person or team accountable for the outcome.

负责最终结果的人。

例如：

> The API gateway is owned by the Platform Team.

不是说 Platform Team 拥有代码。

意思：

Platform Team 负责维护它。

---

## Responsibility

更像组织职责。

例如：

> The security team is responsible for security reviews.

安全团队负责安全审核。

但是：

> Who owns this bug?

比：

> Who is responsible for this bug?

自然。

---

## Assignee

来自 assign：

分配任务。

例如 Jira：

```
Issue:
Payment failure

Owner:
Payment Team

Assignee:
Alice
```

---

## Maintainer

维护者。

特别用于：

- Open Source
- Library
- Repository

例如：

> The maintainer reviewed the pull request.

---

# 2. Accountability（结果负责）

这个词比 responsibility 更进一步。

## Responsibility

我负责做。

## Accountability

我负责结果。

例如：

开发：

> Bob is responsible for implementing the feature.

Bob 写代码。

但是：

> Bob is accountable for the release.

Bob 对上线结果负责。

---

管理层非常喜欢这个词。

常见：

> We need clear accountability.

---

# 3. Assignment（任务分配）

---

## Assign

分配任务。

> Assign this ticket to John.

---

## Delegate

委托。

区别：

Assign:

老板分任务。

Delegate:

把责任授权出去。

例如：

> The manager delegated the task to the engineer.

---

## Ownership transfer

责任转移。

例如：

> Ownership has been transferred to the SRE team.

---

# 4. Issue / Ticket / Task

中文都叫：

问题。

但是工程里面不同。

---

# Issue

最大范围。

可以是：

- bug
- feature request
- question
- improvement

GitHub：

> Open an issue.

---

# Ticket

强调：

流程化管理。

例如：

- Support ticket
- Service ticket

通常意味着：

进入队列。

---

# Task

明确行动。

例如：

> Update API documentation.

---

关系：

```
Issue
 |
 +-- Bug
 |
 +-- Task
 |
 +-- Feature Request
 |
 +-- Question
```

---

# 5. Bug

## 核心

代码导致错误行为。

模型：

```
Expected behavior
        |
        X
Actual behavior
```

---

例如：

> Users cannot reset passwords.

这是 bug。

---

## Bug Fix

修复。

> Fix the authentication bug.

---

## Regression

回归问题。

非常重要。

意思：

以前正常，现在坏了。

例如：

> This release introduced a regression.

---

# 6. Incident（事故）

中文：

故障。

但是比 bug 高一级。

---

Bug：

代码问题。

Incident：

用户受到影响。

例如：

代码：

```
Memory leak
```

可能没有 incident。

但是：

```
Production crashed
```

就是 incident。

---

常见：

> We had a production incident yesterday.

---

# 7. Problem（根因问题）

这是 ITIL / SRE 文化。

关系：

```
Incident
    |
    ↓
Why?
    |
Problem
    |
    ↓
Root Cause
```

---

例：

Incident:

> Website unavailable.

Problem:

> Database connection exhaustion.

Root Cause:

> Connection pool configuration was incorrect.

---

# 8. Root Cause（根因）

不要简单理解：

原因。

工程师喜欢：

root cause。

因为他们不满足：

表面现象。

---

例：

问题：

```
API timeout
```

普通原因：

```
Server slow
```

Root cause:

```
Inefficient database query caused CPU saturation.
```

---

常见：

> We need to identify the root cause.

---

# 9. Reproduce（复现）

软件工程高频词。

中文：

复现 bug。

英文：

reproduce。

---

例如：

> I cannot reproduce the issue.

意思：

我无法在本地再次触发。

---

相关：

## Repro steps

复现步骤。

例如：

> Please provide repro steps.

---

# 10. Workaround（临时方案）

非常工程化。

不是 fix。

---

Fix：

永久解决。

Workaround：

绕过去。

例如：

问题：

上传失败。

Workaround：

改用另一种上传方式。

---

表达：

> We have a temporary workaround.

---

# 11. Mitigation（缓解措施）

比 workaround 更广。

重点：

降低影响。

---

Incident：

服务器压力过大。

Mitigation：

- 限流
- 扩容
- 禁用功能

---

表达：

> We applied a mitigation while investigating the root cause.

---

# 12. Resolution（解决闭环）

中文：

解决。

工程里面：

resolve。

---

不是：

“代码改完”。

而是：

```
Identify
 ↓
Fix
 ↓
Verify
 ↓
Close
```

---

表达：

> The issue has been resolved.

---

# 13. Escalation（升级处理）

中文：

升级。

不是版本升级。

---

意思：

问题升级给更高权限的人。

例如：

客服：

↓

工程：

↓

架构师。

---

表达：

> Escalate the issue to the infrastructure team.

---

# 14. Triage（分诊）

非常典型工程词。

来源：

医疗分诊。

意思：

快速判断：

- 严重程度
- 优先级
- 负责人

---

Bug triage：

```
New Bug

↓
Severity?
Priority?
Owner?
```

---

表达：

> We need to triage incoming issues.

---

# 15. Priority vs Severity

很多人混。

---

## Severity

影响程度。

例如：

系统全部挂掉：

High severity。

---

## Priority

处理顺序。

例如：

老板关注：

High priority。

---

可能：

```
Severity: Low
Priority: High
```

例如：

一个小问题，但是老板要求马上改。

---

# 16. Blocker（阻塞）

非常常用。

意思：

导致无法继续。

---

例如：

> Missing access permission is blocking development.

---

区别：

Dependency：

存在依赖。

Blocker：

已经卡住。

---

# 17. Dependency（依赖）

工程核心概念。

---

A 需要 B。

例如：

```
Frontend
   |
   ↓
Backend API
```

Frontend has dependency on Backend.

---

表达：

> This change has a dependency on the authentication service.

---

# 18. Constraint（约束）

架构讨论高频。

意思：

限制条件。

例如：

- latency requirement
- budget
- compatibility

---

表达：

> The design is constrained by backward compatibility requirements.

---

# 19. Trade-off（权衡）

架构师最爱。

因为工程没有完美方案。

---

例如：

性能 vs 成本：

> There is a trade-off between performance and cost.

---

# 20. Scope（范围）

工程沟通核心。

---

## In scope

包含。

## Out of scope

不包含。

---

设计文档：

```
Scope

This proposal covers...

Out of scope:

...
```

---

# 21. Alignment（对齐）

中文：

达成共识。

不是：

make everyone agree。

---

意思：

大家理解一致。

---

表达：

> Let's align on the approach.

---

# 22. Context（背景）

技术文档非常重要。

不是：

background。

---

RFC：

```
Context
Problem
Proposal
Decision
```

---

Context：

为什么现在讨论这个事情。

---

# 23. Decision（决策）

工程文档常见。

不是：

choice。

---

例如：

> The decision is to migrate to PostgreSQL.

---

# 24. Action Item（行动项）

会议文化。

意思：

会议后明确执行事项。

---

例如：

```
Action Items:

- Alice: update API docs
- Bob: verify migration plan
```

---

# 25. Follow-up（跟进）

非常常用。

---

不是：

催。

而是：

后续动作。

---

表达：

> I'll follow up on this issue.

---

# 这一部分总结：工程师处理一个问题时的大脑流程

真实工程团队思考：

```
Something happened

        ↓

Is it a bug or incident?

        ↓

Who owns it?

        ↓

Who is assigned?

        ↓

Can we reproduce it?

        ↓

What's the root cause?

        ↓

What's the workaround?

        ↓

What's the resolution?

        ↓

How do we prevent recurrence?
```

这套逻辑，就是为什么这些词会出现。

---

下一部分我会继续整理：

**Part 2：Architecture & Code Quality（架构设计和代码质量）**

里面会重点解释：

- abstraction 为什么不是“抽象”
- coupling / cohesion 为什么成对出现
- scalability / extensibility / maintainability 的区别
- technical debt 为什么叫债
- refactor 和 rewrite 的文化差异
- clean code 背后的工程思想
- interface / contract / boundary 为什么这么用

## 这些是写设计文档和参加架构讨论最常用的一批。

# Part 2：Architecture & Code Quality（架构设计与代码质量）

这一部分是软件工程里非常核心的一套语言体系。

和 Part 1 的区别：

Part 1 主要描述：

> **事情怎么被管理、谁负责、怎么推进**

Part 2 描述：

> **代码和系统应该如何设计，为什么这样设计**

这里的很多词，如果只翻译成中文，会非常容易误解。

例如：

- abstraction = 抽象 ❌（中文感觉很玄）
- coupling = 耦合 ❌（很多人知道，但不知道工程师为什么在意）
- boundary = 边界 ❌（不知道边界在哪里）
- contract = 契约 ❌（感觉像法律）
- debt = 债务 ❌（为什么代码会欠债？）

下面逐个拆。

---

# 1. Abstraction（抽象）

这是软件工程最重要的概念之一。

---

## 中文直觉

看到 abstraction：

> 抽象

很多人想到：

“把东西变复杂？”

其实相反。

---

## 工程含义

Abstraction：

> Hide unnecessary details and expose only what users need.

隐藏不重要的细节，只暴露必要接口。

---

例如：

你开车。

你看到：

```text
Steering wheel
Brake pedal
Accelerator
```

你不知道：

- 发动机怎么燃烧
- 变速箱怎么工作
- ECU 怎么控制

这就是 abstraction。

---

软件：

你调用：

```python
send_email()
```

你不关心：

- SMTP
- socket
- retry
- connection pool

---

## 为什么需要 abstraction？

因为复杂度会增长。

没有 abstraction：

```text
User
 |
Database
 |
Network
 |
Storage
 |
Hardware
```

每层都知道下面细节。

结果：

修改困难。

---

有 abstraction：

```text
User

 ↓

Service Interface

 ↓

Database Layer

 ↓

Storage
```

每层只关心接口。

---

## 常见表达：

> We need a higher level of abstraction.

我们需要更高层抽象。

---

> This abstraction leaks implementation details.

这个抽象暴露了底层实现细节。

这个非常高级。

意思：

你的接口设计不好。

---

# 2. Encapsulation（封装）

很多中文开发者知道“封装”。

但英文工程语境更强调：

> Protect internal state from external modification.

---

例如：

不好：

```java
account.balance = -100;
```

外部随便改内部状态。

---

封装：

```java
account.withdraw(amount);
```

内部控制：

- validation
- logging
- permission

---

Abstraction 和 Encapsulation 区别：

|      | Abstraction  | Encapsulation        |
| ---- | ------------ | -------------------- |
| 关注 | 隐藏复杂性   | 保护内部状态         |
| 目的 | 降低理解成本 | 降低修改风险         |
| 例子 | API          | class private fields |

---

# 3. Interface（接口）

很多人理解：

接口 = API。

但是工程文化里更广。

---

## 核心：

Interface:

> A boundary where two components communicate.

两个东西交流的约定。

---

例如：

Frontend：

```javascript
GET / users;
```

Backend：

返回：

```json
{
  "name": "Alice"
}
```

这个协议就是 interface。

---

## Interface 不一定是代码

例如：

团队之间：

Backend Team:

> We provide user data in this format.

这也是 interface。

---

常见：

> Define a clear interface between modules.

---

# 4. Contract（契约）

这个词很有工程味。

---

为什么不用 agreement？

因为 contract 强调：

> If you provide X, I guarantee Y.

---

例如 API contract：

请求：

```json
{
  "userId": 123
}
```

保证：

返回：

```json
{
  "name": "Bob"
}
```

---

所以：

Interface:

“怎么交流”

Contract:

“交流时保证什么”

---

常见：

> The API contract should remain stable.

---

# 5. Boundary（边界）

架构设计里面非常重要。

---

Boundary：

不是物理边界。

而是：

> A separation between responsibilities.

---

例如：

系统：

```text
Frontend

---- Boundary ----

Backend API

---- Boundary ----

Database
```

---

为什么重要？

因为边界决定：

- 谁负责什么
- 谁不能知道什么

---

常见：

> Keep business logic outside the database boundary.

---

# 6. Coupling（耦合）

中文翻译：

耦合。

但很多人不知道为什么工程师害怕它。

---

核心：

> How much one component depends on another.

---

高 coupling：

```text
A ---> B ---> C ---> D
```

A 改动：

影响全部。

---

低 coupling：

```text
A ---> Interface

B ---> Interface

C ---> Interface
```

组件独立。

---

工程目标：

不是 zero coupling。

因为完全没有依赖：

系统无法工作。

目标：

> Loose coupling

---

常见：

> Reduce coupling between services.

---

# 7. Cohesion（内聚）

Coupling 经常一起出现。

---

Cohesion：

> How closely related the responsibilities inside one component are.

---

高 cohesion：

一个模块：

```text
PaymentService

- charge()
- refund()
- validatePayment()
```

都是支付。

---

低 cohesion：

```text
Utils.java

- sendEmail()
- calculateTax()
- resizeImage()
- validateUser()
```

垃圾桶类。

---

目标：

```text
High cohesion
+
Low coupling
```

这是经典架构原则。

---

# 8. Dependency（依赖）

Part 1 讲流程依赖。

这里讲代码依赖。

---

例如：

A 使用 B：

```java
class OrderService {
   PaymentService payment;
}
```

OrderService depends on PaymentService.

---

问题：

依赖越多：

修改越困难。

---

常见：

> Minimize unnecessary dependencies.

---

# 9. Dependency Injection（依赖注入）

非常常见。

---

普通：

```java
class OrderService {

 PaymentService payment =
     new PaymentService();

}
```

自己创建。

---

DI：

别人提供。

```java
OrderService(PaymentService payment)
```

---

为什么？

降低 coupling。

---

表达：

> Dependency injection improves testability.

---

# 10. Separation of Concerns（关注点分离）

非常重要。

---

意思：

不同事情不要混在一起。

---

例如：

Controller:

处理 HTTP。

Service:

业务逻辑。

Repository:

数据库。

不要：

```java
Controller {

 SQL
 Business Logic
 Email
 Logging

}
```

---

常见：

> Separate concerns into different layers.

---

# 11. Layer（层）

架构讨论高频。

例如：

经典：

```text
Presentation Layer

Business Layer

Data Layer
```

---

为什么分层？

控制复杂度。

---

常见：

> Move this logic to the service layer.

---

# 12. Module（模块）

不要简单理解：

文件。

Module：

> A unit of functionality with a clear responsibility.

---

例如：

Authentication module。

里面：

- login
- token
- permission

---

# 13. Component（组件）

比 module 更强调：

可独立组合。

例如：

Frontend component:

Button

Backend component:

Payment Service

---

区别：

Module:

代码组织。

Component:

系统组成。

---

# 14. Service（服务）

微服务时代高频。

---

Service:

提供能力。

例如：

Authentication Service

Payment Service

---

不是：

“服务器”。

Server:

运行程序的机器/进程。

Service:

提供功能。

---

# 15. Scalability（可扩展性）

中文：

扩展性。

但是有多个。

---

Scalability：

> Can handle increasing load?

例如：

用户：

1000

↓

1000000

系统还能工作。

---

常见：

> The system needs to scale horizontally.

---

# 16. Horizontal Scaling vs Vertical Scaling

---

Vertical：

加机器配置。

```text
4 CPU

↓

32 CPU
```

---

Horizontal：

增加机器数量。

```text
1 server

↓

10 servers
```

---

云计算非常常见。

---

# 17. Extensibility（可扩展）

和 scalability 不一样。

---

Extensibility：

增加新功能容易。

例如：

插件系统。

---

Scalability：

处理更多流量。

---

区别：

|          | Extensibility | Scalability |
| -------- | ------------- | ----------- |
| 增加什么 | 功能          | 负载        |
| 问题     | 未来变化      | 当前压力    |

---

# 18. Maintainability（可维护性）

核心指标。

---

意思：

未来的人修改它容易吗？

包括：

- readable code
- simple design
- tests

---

表达：

> Improve maintainability.

---

# 19. Reliability（可靠性）

系统多久正常工作。

---

关注：

failure。

---

例如：

99.9% uptime。

---

# 20. Availability（可用性）

系统是否能访问。

---

区别：

Reliability:

长期可靠。

Availability:

现在能不能用。

---

例如：

系统：

过去一年只挂10分钟。

高 reliability。

---

# 21. Performance（性能）

不要只理解快。

包括：

- latency
- throughput
- resource usage

---

# 22. Latency（延迟）

一次请求花多久。

例如：

> Reduce API latency.

---

# 23. Throughput（吞吐）

单位时间处理多少。

例如：

> Increase request throughput.

---

区别：

Latency：

一个请求。

Throughput：

整体能力。

---

# 24. Optimization（优化）

为什么不要随便说 optimize？

Optimize:

寻找更优解。

例如：

数据库：

> Optimize query performance.

---

不是：

> Optimize the team process.

通常：

improve process。

---

# 25. Refactor（重构）

非常重要。

---

Refactor：

> Change internal structure without changing external behavior.

重点：

行为不变。

---

例如：

旧代码：

```text
works but messy
```

重构：

```text
cleaner structure
```

用户无感。

---

# 26. Rewrite（重写）

完全重新实现。

风险更高。

---

区别：

Refactor:

小步改善。

Rewrite:

推倒重来。

---

工程文化：

通常偏向：

> Refactor incrementally.

---

# 27. Technical Debt（技术债）

非常经典。

为什么叫债？

因为：

现在偷懒：

↓

未来付利息。

---

例如：

今天：

复制代码。

未来：

10处修改。

---

表达：

> We need to pay down technical debt.

注意：

不是 pay off。

工程常说：

pay down debt。

---

# 28. Code Smell（代码异味）

不是 bug。

---

意思：

代码看起来有问题。

例如：

- huge class
- duplicated code

---

表达：

> This is a code smell.

---

# 29. Clean Code（整洁代码）

不是漂亮。

是：

容易：

- understand
- modify
- test

---

# 30. Design Pattern（设计模式）

工程共同语言。

例如：

- Factory
- Singleton
- Observer

---

作用：

不用解释整个设计。

---

# 31. Anti-pattern（反模式）

错误但常见的设计。

例如：

God Object。

---

表达：

> This approach is an anti-pattern.

---

# 32. Over-engineering（过度设计）

非常常用。

---

意思：

为不存在的问题设计复杂方案。

---

表达：

> Avoid over-engineering.

---

# 33. KISS Principle

Keep It Simple, Stupid。

工程文化：

简单优先。

---

# 34. YAGNI

You Aren't Gonna Need It。

意思：

不要提前实现未来可能需要的东西。

---

# 35. DRY

Don't Repeat Yourself。

不要重复。

---

# 36. SOLID

面向对象设计原则。

包括：

- Single Responsibility
- Open/Closed
- Liskov Substitution
- Interface Segregation
- Dependency Inversion

---

# 这一部分总结：架构师脑中的模型

一个成熟工程师讨论设计时：

```text
What is the boundary?

        ↓

What is the interface?

        ↓

What is the contract?

        ↓

Are responsibilities separated?

        ↓

Is coupling low?

        ↓

Is cohesion high?

        ↓

Can it scale?

        ↓

Can we maintain it?

        ↓

What are the trade-offs?
```

这就是为什么英语技术讨论里会高频出现这些词。

---

下一部分我建议继续：

**Part 3：Development Lifecycle & Delivery（研发流程与交付文化）**

会覆盖：

- requirement
- specification
- proposal
- RFC
- implementation
- rollout
- deployment
- release
- rollback
- feature flag
- CI/CD
- pipeline
- build
- artifact
- environment
- staging
- production
- hotfix
- cherry-pick
- branch strategy

## 这些是每天写代码、提 PR、发版时最常用的一套。

---

# Part 3：Development Lifecycle & Delivery（研发流程与交付文化）

这一部分是软件团队每天最常接触的一套语言。

如果 Part 1 是：

> 一个问题怎么被管理

Part 2 是：

> 一个系统怎么被设计

那么 Part 3 是：

> 一个想法怎么变成代码，代码怎么安全地变成线上服务

很多中文开发者的问题是：

知道单词，但是不知道**软件团队的流程模型**。

例如：

- requirement 和 specification 有什么区别？
- build 和 deploy 有什么区别？
- release 和 rollout 为什么不是一个东西？
- staging 和 production 为什么要分环境？
- hotfix 和 patch 有什么文化差异？

下面展开。

---

# 1. Requirement（需求）

这是软件开发的起点。

---

## 中文直觉

需求 = 用户想要什么。

这个理解没错，但是工程里会细分。

---

## Requirement

强调：

> What the system should do.

系统应该提供什么能力。

例如：

用户：

> Users should be able to reset their password.

这是 requirement。

---

## Feature

功能。

通常是 requirement 的实现形式。

例如：

Requirement:

> Users need password recovery.

Feature:

> Add password reset flow.

---

## User Story

敏捷开发常用。

格式：

> As a user, I want X so that Y.

例如：

> As a customer, I want to reset my password so that I can regain access to my account.

---

区别：

|      | Requirement | Feature  | User Story |
| ---- | ----------- | -------- | ---------- |
| 关注 | 需求目标    | 功能实现 | 用户视角   |

---

# 2. Specification（规格说明）

这是非常重要的区别。

很多人把 requirement 和 specification 混在一起。

---

## Requirement

说：

> What do we need?

例如：

用户需要登录。

---

## Specification

说：

> How exactly should it work?

例如：

登录接口：

```
POST /login

Input:
email
password

Output:
token

Error:
401 Unauthorized
```

这就是 specification。

---

简单理解：

```
Requirement
    ↓
Specification
    ↓
Implementation
```

---

常见表达：

> The requirement is clear, but the specification is incomplete.

---

# 3. Design（设计）

中文：

设计。

但是工程里有层次。

---

## High-level Design (HLD)

高层设计。

关注：

- 服务划分
- 架构
- 数据流

例如：

```
Frontend

↓

API Gateway

↓

Backend Services

↓

Database
```

---

## Low-level Design (LLD)

低层设计。

关注：

- class
- function
- database schema

---

区别：

|      | HLD  | LLD  |
| ---- | ---- | ---- |
| 范围 | 系统 | 代码 |

---

# 4. Proposal（方案提议）

工程沟通非常常见。

---

Proposal：

> A suggested approach for discussion.

不是最终决定。

例如：

> I propose using Redis for caching.

意思：

我提出一个方案。

---

相关：

## Alternative

备选方案。

> Another alternative is using Memcached.

---

## Recommendation

推荐。

> Our recommendation is Redis.

---

## Decision

最终决定。

> The decision is to use Redis.

---

关系：

```
Proposal
    ↓
Discussion
    ↓
Decision
```

---

# 5. RFC（Request for Comments）

非常重要的工程文化。

很多大公司都有。

---

名字容易误解：

不是：

“请求评论”。

实际：

> A document proposing a technical change for review.

---

用途：

大型技术决定。

例如：

- 新架构
- API 变化
- 基础设施改造

---

典型结构：

```
Title

Context

Problem

Proposal

Alternatives

Trade-offs

Decision
```

---

为什么需要 RFC？

因为：

> Important decisions should not happen only in meetings.

让：

- 背景留下
- 讨论留下
- 决策留下

---

# 6. Implementation（实现）

中文：

实现。

---

意思：

把设计变成代码。

---

常见：

> The implementation is straightforward.

---

注意：

Implementation 不等于 coding。

包括：

- code
- configuration
- tests
- integration

---

# 7. Development（开发）

很宽。

包括：

设计：

↓

编码：

↓

测试。

---

例如：

> The feature is under development.

---

# 8. Build（构建）

很多人和 deploy 混。

---

Build：

把代码变成可运行产物。

例如：

源码：

```
main.java
```

↓

编译

↓

```
app.jar
```

这个过程：

build。

---

常见：

> The build failed.

意思：

构建失败。

---

# 9. Artifact（构建产物）

非常工程化。

---

Artifact：

> The output produced by a build process.

例如：

- jar
- docker image
- binary
- package

---

关系：

```
Source Code

↓

Build

↓

Artifact

↓

Deploy
```

---

表达：

> The pipeline generated a Docker image artifact.

---

# 10. Package（打包）

---

把代码和依赖组合。

例如：

npm package

Python package

---

注意：

package 也可以表示软件包。

---

# 11. Deploy（部署）

中文：

部署。

---

Deploy：

把软件放到运行环境。

例如：

```
Local

↓

Staging

↓

Production
```

---

表达：

> Deploy the service to production.

---

# 12. Release（发布）

这个词经常和 deploy 混。

---

Release：

> Make a version available to users.

---

Deploy：

技术动作。

Release：

产品动作。

---

例如：

代码已经 deploy 到服务器：

但是：

没有开放给用户。

还不是 release。

---

关系：

```
Build

↓

Deploy

↓

Release
```

---

# 13. Rollout（逐步发布）

非常重要。

---

Release：

全部上线。

Rollout：

逐渐扩大范围。

---

例如：

第一天：

```
5% users
```

第二天：

```
50%
```

最后：

```
100%
```

---

表达：

> We will roll out the feature gradually.

---

# 14. Rollback（回滚）

上线失败时。

---

意思：

恢复到之前版本。

---

例如：

```
Version 2.0
     ↓
Problem
     ↓
Rollback
     ↓
Version 1.9
```

---

表达：

> We need to rollback the deployment.

---

# 15. Hotfix（紧急修复）

生产环境紧急问题。

---

特点：

- 快
- 小范围
- 高优先级

---

例如：

支付挂了。

马上：

> Deploy a hotfix.

---

区别：

Regular fix：

正常开发流程。

Hotfix：

生产救火。

---

# 16. Patch（补丁）

比 hotfix 更广。

---

Patch：

一个修复变更。

例如：

security patch。

---

Hotfix：

特殊场景的 patch。

---

关系：

```
Patch

 +-- Bug fix patch
 +-- Security patch
 +-- Hotfix
```

---

# 17. Version（版本）

工程基础。

---

例如：

```
v1.2.3
```

---

语义版本：

Semantic Versioning：

```
Major.Minor.Patch
```

例如：

```
2.5.1
```

---

# 18. Breaking Change（破坏性变化）

非常重要。

---

意思：

旧用户无法继续使用。

例如：

以前：

```
GET /user?id=1
```

改成：

```
GET /users/1
```

旧客户端坏。

---

表达：

> This is a breaking change.

---

# 19. Backward Compatibility（向后兼容）

工程文化非常重视。

---

意思：

新版本支持旧使用方式。

---

例如：

旧 API：

```
v1
```

新 API：

```
v2
```

仍支持 v1。

---

表达：

> Maintain backward compatibility.

---

# 20. Feature Flag（功能开关）

现代工程非常常见。

---

不是：

发布 = 用户看到。

通过开关控制。

例如：

代码已经上线：

```
if feature_enabled:
    show_new_ui
```

---

优势：

- 灰度
- A/B test
- 快速关闭

---

表达：

> Enable the feature flag for internal users first.

---

# 21. Environment（环境）

软件工程核心概念。

常见：

```
Development

↓

Testing

↓

Staging

↓

Production
```

---

# 22. Development Environment

开发环境。

工程师自己使用。

---

# 23. Test Environment

测试环境。

自动测试或 QA。

---

# 24. Staging Environment

非常重要。

---

Staging：

> Production-like environment for final validation.

接近生产。

用于：

上线前检查。

---

# 25. Production Environment

线上真实环境。

简称：

prod。

---

表达：

> The issue only happens in production.

---

# 26. CI（Continuous Integration）

持续集成。

核心：

代码经常合并。

流程：

```
Code Commit

↓

Build

↓

Test

↓

Feedback
```

---

目标：

早点发现问题。

---

# 27. CD（Continuous Delivery / Deployment）

两个 CD。

---

## Continuous Delivery

持续交付。

代码随时可以发布。

---

## Continuous Deployment

持续部署。

自动发布。

---

区别：

Delivery：

准备好。

Deployment：

自动上线。

---

# 28. Pipeline（流水线）

CI/CD 核心。

---

例如：

```
Commit

↓

Build

↓

Test

↓

Security Scan

↓

Deploy
```

---

表达：

> The CI pipeline failed.

---

# 29. Automation（自动化）

工程文化关键词。

---

目的：

减少人工。

---

例如：

> Automate repetitive tasks.

---

# 30. Manual Intervention（人工干预）

自动化的反面。

---

例如：

> The deployment requires manual approval.

---

# 31. Approval（审批）

企业环境常见。

---

例如：

生产发布：

```
Developer

↓

Reviewer

↓

Approval

↓

Deploy
```

---

# 32. Code Freeze（代码冻结）

发布前停止改动。

---

例如：

大版本发布。

表达：

> We are entering code freeze.

---

# 33. Branch Strategy（分支策略）

Git 文化。

---

## Branch

代码分支。

---

## Main / Master

主分支。

---

## Feature Branch

功能分支。

---

## Release Branch

发布分支。

---

## Hotfix Branch

紧急修复分支。

---

# 34. Merge（合并）

多个分支合并。

---

# 35. Rebase（变基）

重新整理提交历史。

---

# 36. Cherry-pick（挑选提交）

非常工程化。

意思：

把某一个 commit 拿过来。

例如：

> Cherry-pick the fix into the release branch.

---

# 37. Commit（提交）

代码变更单位。

---

不是：

保存。

而是：

一个有意义的修改记录。

---

好的 commit：

> Add retry logic for API timeout

坏：

> update code

---

# 38. Pull Request / Merge Request

代码审核流程。

---

目的：

- review
- discussion
- approval

---

# 39. Code Review

不是找错。

更重要：

- design discussion
- knowledge sharing

---

# 40. Review Comment 文化

常见：

---

## Suggestion

建议。

---

## Nit

小问题。

例如：

> Nit: Rename this variable.

---

## Blocking Comment

必须修改。

---

# 41. Testing 相关

---

## Unit Test

测试单个组件。

---

## Integration Test

测试组件协作。

---

## End-to-End Test

模拟用户流程。

---

关系：

```
Unit

↓

Integration

↓

E2E
```

---

# 42. Regression Test

回归测试。

确认：

旧功能没有坏。

---

# 43. Test Coverage

测试覆盖率。

---

不是质量本身。

高 coverage ≠ 高质量。

---

# 44. Flaky Test

非常工程化。

意思：

偶尔失败。

---

例如：

今天通过：

明天失败。

---

表达：

> We need to fix flaky tests.

---

# 45. CI/CD Pipeline 的完整模型

一个成熟团队：

```
Developer

↓

Commit

↓

Pull Request

↓

Code Review

↓

CI Pipeline

    |
    +-- Build
    |
    +-- Unit Test
    |
    +-- Integration Test
    |
    +-- Security Scan

↓

Artifact

↓

Deploy to Staging

↓

Validation

↓

Rollout to Production

↓

Monitor

```

---

# 这一部分总结：工程师脑中的交付模型

他们不是想：

> 写代码 → 上线

而是：

```
Requirement

↓

Specification

↓

Design

↓

Implementation

↓

Review

↓

Build

↓

Test

↓

Deploy

↓

Release

↓

Monitor

↓

Improve
```

---

这些词为什么重要？

因为英语工程沟通不是描述动作，而是在描述**软件生命周期里的状态变化**。

比如：

中文：

> 这个功能做好了。

工程英语：

根据状态不同：

- implemented（代码完成）
- reviewed（审核完成）
- built（构建完成）
- deployed（部署完成）
- released（用户可用）
- rolled out（逐步开放）

这就是为什么工程英语需要理解背后的流程。

---

下一部分会是：

# Part 4：SRE / Production / Reliability（运维、稳定性、线上事故文化）

这一部分会解释：

- reliability vs availability vs resilience
- monitoring vs observability
- log / metric / trace
- alert / alarm
- incident / outage / degradation
- postmortem
- RCA
- SLA / SLO / SLI
- capacity planning
- scaling
- failover
- disaster recovery
- graceful degradation

## 这一批词是大型互联网公司技术沟通里非常高频的。

# Part 4：SRE / Production / Reliability（运维、稳定性、线上事故文化）

这一部分是现代软件工程（尤其互联网、大规模系统）非常重要的一套语言。

如果前面：

- Part 1：**怎么管理问题**
- Part 2：**怎么设计系统**
- Part 3：**怎么交付软件**

那么 Part 4：

> **系统上线以后，如何保证它可靠运行？出了问题如何处理？**

这里的词汇非常体现工程文化。

很多中文开发者会说：

> 服务挂了 → 修一下

但成熟工程团队的思考方式是：

```text
Something happened

↓

How severe is it?

↓

What is the impact?

↓

How do we detect it?

↓

How do we mitigate it?

↓

What is the root cause?

↓

How do we prevent recurrence?
```

---

# 1. Reliability（可靠性）

这是 SRE 最核心的词。

---

## 中文：

可靠性。

但是不要简单理解：

“不容易坏”。

---

## 工程定义：

> The ability of a system to perform correctly over time.

系统长期正确运行的能力。

关注：

- failure frequency
- consistency
- correctness

---

例如：

一个支付系统：

今天能支付：

不代表可靠。

可靠：

一年内：

- 少失败
- 数据正确
- 行为稳定

---

常见：

> Improve system reliability.

提升系统可靠性。

---

# 2. Availability（可用性）

经常和 reliability 混。

---

## Availability：

> Is the system available when users need it?

用户现在能不能访问。

---

例如：

网站：

99.9% 时间可访问。

这是 availability。

---

## 区别：

|      | Reliability  | Availability |
| ---- | ------------ | ------------ |
| 关注 | 长期正确运行 | 现在能不能用 |
| 问题 | 会不会坏     | 有没有挂     |

---

一个系统：

可能：

availability 高：

一直在线。

但是：

reliability 差：

偶尔返回错误数据。

---

# 3. Resilience（韧性）

这是近几年非常流行的词。

---

## 含义：

> Ability to recover from failures and continue operating.

面对故障还能继续工作。

---

例如：

数据库挂了：

普通系统：

```text
Database down

↓

Service down
```

Resilient system：

```text
Database down

↓

Failover

↓

Continue service
```

---

常见：

> Build resilient systems.

---

# 4. Fault Tolerance（容错）

和 resilience 接近。

---

## Fault Tolerance：

系统允许部分故障。

例如：

三个服务器：

```text
Server A ❌

Server B ✅

Server C ✅
```

用户无感。

---

区别：

|      | Fault tolerance | Resilience |
| ---- | --------------- | ---------- |
| 重点 | 承受故障        | 恢复能力   |

---

# 5. Failure（失败）

工程里面非常普通。

---

不是：

“失败了”。

而是：

组件没有达到预期行为。

---

例如：

- service failure
- network failure
- database failure

---

表达：

> The service failed unexpectedly.

---

# 6. Outage（中断）

线上非常常用。

---

## Outage：

服务不可用。

例如：

网站打不开。

---

表达：

> We experienced a production outage.

---

区别：

Failure:

组件失败。

Outage:

用户感知的不可用。

---

关系：

```text
Component Failure

        ↓

Service Outage

        ↓

User Impact
```

---

# 7. Degradation（降级）

非常重要。

---

不是完全挂。

而是：

性能或功能下降。

---

例如：

正常：

```text
Search returns in 100ms
```

降级：

```text
Search returns in 3s
```

---

表达：

> The service is experiencing performance degradation.

---

# 8. Graceful Degradation（优雅降级）

高级工程词。

---

意思：

失败时，不是全部崩。

例如：

图片服务挂了：

不好：

```text
Page Error
```

好：

```text
Show placeholder image
```

---

表达：

> Support graceful degradation.

---

# 9. Monitoring（监控）

最基础。

---

## Monitoring：

观察系统状态。

例如：

CPU：

Memory：

Request count：

---

表达：

> Monitor system metrics.

---

但是现代工程更常说：

Observability。

---

# 10. Observability（可观测性）

非常重要。

---

中文：

可观测性。

但是含义比监控大。

---

Monitoring 问：

> Is something wrong?

Observability 问：

> Why is it wrong?

---

例如：

CPU 100%。

Monitoring：

发现 CPU 高。

Observability：

找到：

哪个请求？

哪个服务？

哪个代码？

导致 CPU 高。

---

经典三大支柱：

```text
Observability

 |
 +-- Logs
 |
 +-- Metrics
 |
 +-- Traces
```

---

# 11. Log（日志）

---

记录事件。

例如：

```text
User login failed
```

---

用途：

查看历史。

---

问题：

日志告诉你：

发生了什么。

---

# 12. Metric（指标）

---

数字化数据。

例如：

```
CPU usage: 80%

Request count: 10000/min

Error rate: 2%
```

---

用途：

趋势分析。

---

# 13. Trace（链路追踪）

这里和 Part 1 的 trace 对应。

---

分布式系统：

一次请求：

```text
User

↓

API Gateway

↓

Order Service

↓

Payment Service

↓

Database
```

Trace 可以看到：

每一步耗时。

---

表达：

> Trace the request flow.

---

# 14. Dashboard（仪表盘）

展示系统状态。

例如：

Grafana dashboard。

---

用途：

快速判断：

- 健康状态
- 趋势
- 异常

---

# 15. Alert（告警）

---

系统主动通知。

例如：

```text
Error rate > 5%

↓

Alert
```

---

注意：

Alert ≠ Alarm。

---

# 16. Alarm（报警）

更偏传统监控。

例如：

消防报警。

软件工程现在更喜欢：

alert。

---

因为：

Alert：

需要判断和处理。

Alarm：

强调紧急声音。

---

# 17. Incident Response（事故响应）

线上事故处理流程。

---

不是：

修 bug。

而是：

完整流程。

---

包括：

```text
Detection

↓

Triage

↓

Mitigation

↓

Resolution

↓

Postmortem
```

---

# 18. Incident Commander（事故负责人）

大型团队常用。

---

简称：

IC。

---

不是：

写代码的人。

而是：

协调所有人的人。

---

负责：

- communication
- prioritization
- decision making

---

表达：

> Alice will act as the incident commander.

---

# 19. Severity（严重等级）

事故分类。

---

例如：

```text
SEV-1

SEV-2

SEV-3
```

---

SEV：

Severity。

---

例：

SEV-1：

全球服务不可用。

---

# 20. Impact（影响）

事故分析核心。

---

不要只问：

哪里坏了？

问：

影响谁？

---

例如：

> What is the user impact?

---

可能：

- 100 users
- 10% traffic
- payment unavailable

---

# 21. Mitigation（缓解）

Part 1 提过。

线上尤其重要。

---

目标：

先降低影响。

不是马上找到根因。

---

例如：

问题：

数据库压力过高。

Mitigation：

- disable expensive feature
- increase capacity

---

表达：

> We are focusing on mitigation first.

---

# 22. Root Cause Analysis (RCA)

事故复盘核心。

---

不是：

找到犯错的人。

而是：

找到系统原因。

---

经典：

Five Whys。

例如：

为什么网站挂？

↓

数据库失败。

为什么数据库失败？

↓

连接太多。

为什么连接太多？

↓

没有限制。

---

表达：

> Conduct an RCA after the incident.

---

# 23. Postmortem（事故复盘）

非常工程文化。

---

名字容易误解：

不是：

“尸检”。

虽然来源类似。

---

工程含义：

事故结束后的学习文档。

---

通常包含：

```text
Summary

Impact

Timeline

Root Cause

Resolution

Action Items
```

---

重点：

Blameless。

---

# 24. Blameless（无责文化）

非常重要。

---

意思：

不要寻找：

“谁犯错”。

寻找：

“为什么系统允许错误发生”。

---

例如：

错误：

工程师删除数据库。

成熟文化：

问：

为什么没有：

- permission control?
- backup?
- review?

---

表达：

> We follow a blameless postmortem process.

---

# 25. SLA（Service Level Agreement）

服务等级协议。

---

通常：

对外承诺。

例如：

> 99.9% uptime

---

客户：

“你保证什么？”

---

# 26. SLI（Service Level Indicator）

指标。

---

实际测量。

例如：

```text
Request latency

Error rate

Availability
```

---

# 27. SLO（Service Level Objective）

目标。

---

例如：

SLI：

当前：

99.95% uptime

SLO：

目标：

99.9% uptime

---

关系：

```text
SLI

(actual measurement)

↓

SLO

(target)

↓

SLA

(customer commitment)
```

---

# 28. Error Budget（错误预算）

SRE 非常经典。

---

如果目标：

99.9% uptime

允许：

0.1% 时间失败。

这就是：

error budget。

---

为什么？

因为：

不能为了稳定完全停止开发。

---

表达：

> We have consumed most of our error budget.

---

# 29. Capacity Planning（容量规划）

提前考虑：

未来负载。

---

例如：

双十一：

预计：

10 倍流量。

---

表达：

> We need capacity planning before the launch.

---

# 30. Scaling（扩展）

---

## Scale up

增加机器能力。

例如：

8 CPU → 32 CPU

---

## Scale out

增加机器数量。

例如：

1 server → 20 servers

---

# 31. Load（负载）

系统压力。

---

例如：

CPU load

traffic load

---

表达：

> The service is under heavy load.

---

# 32. Bottleneck（瓶颈）

非常高频。

---

系统中限制性能的地方。

例如：

数据库：

```text
API fast

↓

Database slow
```

Database 是 bottleneck。

---

# 33. Throughput（吞吐）

处理能力。

---

例如：

requests per second。

---

# 34. Latency（延迟）

单次请求时间。

---

例如：

P99 latency。

---

# 35. Timeout（超时）

---

系统等待时间超过限制。

---

表达：

> The request timed out.

---

# 36. Retry（重试）

失败后再次尝试。

---

注意：

无限 retry 会造成问题。

---

常见：

> Add exponential backoff retry.

---

# 37. Failover（故障转移）

自动切换备用。

---

例如：

主数据库：

↓

备用数据库

---

表达：

> Automatic failover is enabled.

---

# 38. Backup（备份）

数据保护。

---

# 39. Restore（恢复）

从备份恢复。

---

区别：

Backup：

保存。

Restore：

拿回来。

---

# 40. Disaster Recovery（灾难恢复）

简称：

DR。

---

面对：

- 数据中心故障
- 大规模灾害

---

包括：

- backup
- failover
- recovery plan

---

# 41. Runbook（运行手册）

运维非常重要。

---

写：

遇到什么问题：

执行什么步骤。

例如：

```
If database is unavailable:

1. Check status

2. Switch traffic

3. Notify team
```

---

# 42. Playbook（操作策略）

比 runbook 更广。

---

Runbook：

具体步骤。

Playbook：

处理某类情况的方法。

---

# 43. Production Readiness（生产准备）

上线前检查。

---

包括：

- monitoring
- alerting
- rollback plan
- capacity

---

表达：

> The service is not production-ready yet.

---

# 44. Health Check（健康检查）

系统检查。

---

例如：

```text
GET /health
```

---

# 45. Availability Zone / Region

云计算常见。

---

Region：

区域。

例如：

Tokyo Region。

---

Availability Zone：

区域内独立故障域。

---

用于：

提高 resilience。

---

# 46. Service Dependency（服务依赖）

微服务环境高频。

---

例如：

```text
Order Service

depends on

Payment Service
```

---

问题：

依赖太多：

系统脆弱。

---

# 47. Blast Radius（影响范围）

非常工程化。

---

字面：

爆炸半径。

意思：

一次故障影响范围。

---

例如：

一个配置错误：

影响全部用户。

Blast radius 很大。

---

工程目标：

> Minimize blast radius.

---

# 48. Canary Release（金丝雀发布）

逐步发布。

类似 rollout。

---

例如：

先给：

1% 用户。

观察。

再扩大。

---

# 49. Blue-Green Deployment（蓝绿部署）

两套环境。

```text
Blue:
Current version

Green:
New version
```

切流量。

---

# 50. Feature Rollback

功能回退。

通常：

feature flag disable。

---

# 这一部分总结：SRE 工程师脑中的模型

一个成熟团队面对线上问题：

```text
User Impact

↓

Severity

↓

Incident Response

↓

Mitigation

↓

Root Cause Analysis

↓

Postmortem

↓

Action Items

↓

Prevent Recurrence
```

---

# 这一批词的核心不是“运维英语”

而是一套工程文化：

普通表达：

> 网站挂了，赶紧修。

工程表达：

> We are experiencing a SEV-1 incident.
> The team is working on mitigation.
> We are investigating the root cause.
> A postmortem will be conducted after resolution.

---

这就是为什么很多国外技术团队沟通听起来“专业”，不是因为用了难词，而是因为他们共享了一套**系统可靠性模型**。

---

下一部分：

# Part 5：Engineering Communication & Project Management（技术沟通、会议、设计讨论文化）

会覆盖：

- alignment
- context
- assumption
- constraint
- concern
- feedback
- suggestion
- discussion
- decision
- action item
- follow-up
- risk
- dependency
- milestone
- timeline
- estimate
- commitment
- priority
- trade-off
- stakeholder
- escalation

## 这一部分非常接近真实跨国团队每天 Slack / Meeting / Design Review 使用的英语。

# Part 5：Engineering Communication & Project Management（技术沟通、会议、项目协作文化）

这一部分其实是很多工程师最容易卡住的地方。

因为技术英语不只是：

- API
- database
- algorithm

真正进入国际团队以后，大量沟通发生在：

- Slack
- Teams
- Jira
- Design Review
- Architecture Meeting
- Planning Meeting
- Incident Meeting

这里使用的是一种**工程协作语言**。

它的核心不是“说得高级”，而是：

> 如何准确表达状态、风险、不确定性、决策和责任。

---

# 1. Context（背景）

这是技术沟通里面最重要的词之一。

---

## 中文感觉

背景。

很多人会写：

> Background

也可以，但是工程文档更喜欢：

> Context

---

## 为什么？

Background：

偏：

“故事背景”。

Context：

强调：

> 当前讨论为什么发生，以及理解问题需要哪些信息。

---

例如：

设计文档：

不好：

```
Background:
Our system is old.
```

更工程：

```
Context:
The current authentication system cannot support multi-region deployment.
```

---

Context 回答：

> Why are we discussing this now?

---

常见：

> Let's provide some context first.

先介绍一下背景。

---

# 2. Assumption（假设）

工程设计里非常常见。

---

## 为什么需要这个词？

因为技术方案永远基于一些前提。

例如：

设计：

> We assume traffic will grow 10x next year.

这个假设如果错：

整个设计可能错。

---

常见：

> This design is based on the following assumptions.

---

## Assumption vs Fact

区别：

Fact:

已经确定。

Assumption:

暂时认为。

---

例如：

Fact:

> Current traffic is 1000 requests/sec.

Assumption:

> Traffic will double next year.

---

# 3. Constraint（约束）

Part 2 提过，但是这里从沟通角度看。

---

工程讨论不是：

“我喜欢这个方案”。

而是：

“受到什么限制”。

---

Constraint 可能来自：

- 技术
- 时间
- 成本
- 法规
- 兼容性

---

例如：

> The main constraint is backward compatibility.

---

# 4. Requirement（需求）

项目沟通核心。

---

但是工程师会区分：

## Business Requirement

业务需求。

例如：

> Reduce checkout abandonment.

---

## Technical Requirement

技术要求。

例如：

> API latency must be below 200ms.

---

## Non-functional Requirement (NFR)

非功能需求。

例如：

- performance
- security
- scalability

---

# 5. Scope（范围）

项目管理高频。

---

核心：

> What is included and what is not included.

---

常见：

## In Scope

包含。

## Out of Scope

不包含。

---

设计讨论：

> This is out of scope for the current phase.

非常常见。

---

# 6. Goal vs Objective

中文：

目标。

但是英文有区别。

---

## Goal

大方向。

例如：

> Improve system reliability.

---

## Objective

具体目标。

例如：

> Reduce API error rate from 2% to 0.1%.

---

关系：

```
Goal

↓

Objectives

↓

Tasks
```

---

# 7. Milestone（里程碑）

项目节点。

---

不是 deadline。

例如：

项目：

```
Jan:
Architecture Design

Feb:
Implementation

Mar:
Release
```

这些都是 milestones。

---

表达：

> The next milestone is beta release.

---

# 8. Timeline（时间线）

---

描述：

事情什么时候发生。

---

例如：

> Here is the proposed timeline.

---

区别：

Timeline:

整体计划。

Deadline:

最后期限。

---

# 9. Estimate（估算）

工程文化非常重要。

---

不是：

猜。

而是：

基于信息预测。

---

例如：

> The implementation estimate is two weeks.

---

## Estimate vs Commitment

非常重要。

---

Estimate：

预计。

Commitment：

承诺。

---

例如：

工程师：

> I estimate this will take two weeks.

不等于：

> I commit to finish in two weeks.

---

为什么？

因为：

软件开发有不确定性。

---

# 10. Effort（工作量）

不要总说：

time。

---

工程师经常估：

effort。

---

例如：

> This task requires significant engineering effort.

---

Time：

日历时间。

Effort：

投入多少工作。

---

一个任务：

可能：

Effort:
5 engineer-days

Timeline:
3 weeks

---

# 11. Priority（优先级）

---

决定：

先做什么。

---

例如：

P0:

最高。

P1:

重要。

P2:

普通。

---

表达：

> We need to prioritize this issue.

---

# 12. Urgency（紧急程度）

和 priority 不一样。

---

Urgency：

多久必须处理。

Priority：

重要程度。

---

例：

一个：

低价值但是今天必须修。

可能：

Low priority

High urgency

---

# 13. Risk（风险）

工程沟通核心。

---

Risk：

未来可能发生的问题。

---

例如：

> The main risk is database migration failure.

---

Risk 不是：

Problem。

---

区别：

Problem:

已经发生。

Risk:

可能发生。

---

# 14. Concern（担忧）

技术讨论非常常见。

---

不是：

反对。

而是：

提出风险。

---

例如：

> My main concern is scalability.

---

这比：

> This design is bad.

专业很多。

---

# 15. Trade-off（权衡）

Part 2 提过。

项目沟通也大量使用。

---

例如：

> This approach reduces cost but increases complexity.

---

工程师不会寻找：

perfect solution。

而讨论：

trade-off。

---

# 16. Option（方案选项）

讨论设计时常见。

---

例如：

```
Option A:
Use Redis

Option B:
Use Memcached
```

---

Option 不是：

选择。

而是：

候选方案。

---

# 17. Alternative（替代方案）

和 option 接近。

---

Alternative:

已经存在的另一种路径。

---

例如：

> An alternative approach is using asynchronous processing.

---

# 18. Recommendation（推荐）

工程讨论最后常出现。

---

例如：

> Our recommendation is Option A.

---

注意：

Recommendation ≠ Decision。

---

# 19. Decision（决策）

最终确定。

---

例如：

> The decision is to migrate to Kubernetes.

---

设计文档：

通常记录：

为什么做这个 decision。

---

# 20. Rationale（理由）

非常工程化。

---

不是：

reason。

---

Rationale：

决策背后的逻辑。

---

例如：

> The rationale behind this decision is scalability.

---

Decision:

做什么。

Rationale:

为什么。

---

# 21. Feedback（反馈）

工程文化高频。

---

Code review：

> Please provide feedback.

---

但是注意：

Feedback 不一定是批评。

包括：

- suggestion
- concern
- approval

---

# 22. Suggestion（建议）

---

比：

"You should..."

柔和。

---

例如：

> I have a suggestion regarding the API design.

---

# 23. Comment（评论）

代码 review 里面：

comment。

---

不是：

普通聊天。

---

例如：

> I left some comments on the PR.

---

# 24. Clarification（澄清）

非常重要。

---

工程师经常说：

> Could you clarify this requirement?

---

意思：

信息不足，需要明确。

---

不是：

质疑。

---

# 25. Confirm（确认）

---

确认事实。

例如：

> Can you confirm the expected behavior?

---

# 26. Verify（验证）

工程领域非常常用。

---

Confirm：

确认信息。

Verify：

通过检查证明。

---

例如：

用户：

> Is this fixed?

工程：

> We need to verify it in staging.

---

# 27. Validate（验证有效性）

和 verify 接近。

---

Validate：

确认是否满足需求。

---

例如：

> Validate the design with users.

---

区别：

Verify：

做对了吗？

Validate：

做的是不是正确的东西？

---

经典：

```
Verification:
Are we building the system right?

Validation:
Are we building the right system?
```

---

# 28. Review（评审）

工程文化核心。

---

包括：

- code review
- design review
- architecture review

---

目的：

不是找错。

而是：

- improve quality
- share knowledge

---

# 29. Approval（批准）

---

表示：

正式认可。

例如：

> Waiting for approval.

---

# 30. Consensus（共识）

---

团队决策常用。

---

不是：

所有人喜欢。

而是：

大家接受方案。

---

表达：

> We need to reach consensus.

---

# 31. Alignment（对齐）

比 consensus 更常用。

---

Alignment：

大家理解一致。

---

例如：

会议开始：

> Let's align on the goals first.

---

# 32. Stakeholder（利益相关者）

项目管理高频。

---

不是：

股东。

这里：

任何受影响的人。

包括：

- users
- product managers
- engineers
- customers

---

表达：

> We need stakeholder feedback.

---

# 33. Escalation（升级）

Part 1 提过。

这里看管理。

---

当问题超过当前团队能力：

↓

升级。

---

例如：

> Escalate this issue to the security team.

---

# 34. Dependency（依赖）

项目管理里面：

依赖别人。

---

例如：

Frontend:

等待：

Backend API。

---

表达：

> This task has an external dependency.

---

# 35. Blocker（阻塞）

---

Dependency 导致无法继续。

---

例如：

> The missing API documentation is blocking development.

---

# 36. Status Update（状态更新）

日常沟通高频。

---

例如：

Daily standup:

```
Yesterday:
Completed X

Today:
Working on Y

Blockers:
None
```

---

# 37. Progress（进展）

---

不要只说：

working。

---

例如：

> We made good progress on the migration.

---

# 38. Update（更新）

非常万能。

---

可以是：

- 状态更新
- 信息更新
- 代码更新

---

例如：

> Any updates on this issue?

---

# 39. Follow-up（跟进）

---

事情没有结束。

---

例如：

> I'll follow up with the team.

---

# 40. Action Item（行动项）

会议文化核心。

---

必须：

谁 + 做什么。

例如：

```
Action Items:

Alice:
Update API documentation

Bob:
Review migration plan
```

---

# 41. Ownership Transfer（责任转移）

跨团队非常常见。

---

例如：

> Ownership will move from Team A to Team B.

---

# 42. Escalate vs Raise

两个容易混。

---

## Raise a concern

提出担忧。

例如：

> I want to raise a concern about security.

---

## Escalate an issue

升级处理。

例如：

> Escalate the issue to management.

---

# 43. Agree / Disagree

工程文化里：

不直接说：

I don't like it。

而：

> I have a different perspective.

---

或者：

> I don't think this addresses the main concern.

---

# 44. Push back（提出异议）

非常真实的团队语言。

---

不是拒绝。

意思：

提出反对意见。

---

例如：

> I want to push back on this approach.

---

# 45. Challenge（挑战）

---

技术讨论常用。

---

例如：

> Let's challenge this assumption.

意思：

重新检查这个假设。

---

# 46. Surface（暴露）

非常工程化。

---

例如：

> This discussion surfaced several issues.

意思：

讨论发现了一些问题。

---

# 47. Identify（识别）

---

发现。

例如：

> Identify potential risks.

---

# 48. Address（处理）

非常高频。

---

中文容易翻：

地址。

实际：

解决/处理。

---

例如：

> We need to address this issue.

---

# 49. Resolve vs Address

区别：

Address:

开始处理。

Resolve:

完全解决。

---

例如：

> We addressed the performance concern.

可能：

已经采取措施。

> We resolved the performance issue.

已经解决。

---

# 50. Ensure（确保）

技术文档超级常见。

---

例如：

> Ensure backward compatibility.

---

不是：

hope。

而是：

采取措施保证。

---

# 51. Avoid（避免）

---

例如：

> Avoid unnecessary complexity.

---

# 52. Consider（考虑）

工程讨论高频。

---

例如：

> We should consider another approach.

---

# 53. Evaluate（评估）

比 consider 更正式。

---

例如：

> Evaluate the performance impact.

---

# 54. Investigate（调查）

---

问题分析。

---

例如：

> We are investigating the issue.

---

# 55. Explore（探索）

---

还没有确定。

---

例如：

> Explore possible solutions.

---

# 56. Decide vs Determine

---

## Decide

做决定。

## Determine

通过分析确定。

---

例如：

> We need to determine the root cause.

> We need to decide the approach.

---

# 57. Communicate（沟通）

工程文化非常重视。

---

不仅：

说。

还包括：

- status
- risk
- decision

---

# 58. Transparency（透明）

这里和 visibility 对比。

---

团队：

> We value transparency.

---

意思：

信息公开。

---

# 59. Accountability（负责）

再次出现。

---

项目管理：

> Someone needs to be accountable for this deliverable.

---

# 60. Commitment（承诺）

非常重要。

---

工程团队：

不要轻易承诺。

---

例如：

> Are we comfortable making this commitment?

---

# 这一部分总结：工程会议中的真实思维链

成熟团队讨论一个项目：

```text
Context

↓

Requirements

↓

Constraints

↓

Options

↓

Trade-offs

↓

Risks

↓

Recommendation

↓

Decision

↓

Action Items

↓

Follow-up
```

---

所以技术英语沟通的核心不是：

“说复杂的英文”。

而是：

**用固定词汇准确表达工程状态。**

例如：

普通：

> 我觉得这个方案有问题。

工程：

> I have some concerns about scalability and maintainability.

普通：

> 这个事情没人负责。

工程：

> There is no clear ownership for this task.

普通：

> 我们需要讨论一下。

工程：

> Let's align on the approach and discuss the trade-offs.

---

下一部分是最后一个大块：

# Part 6：Open Source / Git / Engineering Culture（开源、Git、代码协作文化）

会包含：

- repository
- commit
- branch
- merge
- rebase
- cherry-pick
- fork
- upstream
- contributor
- maintainer
- convention
- style guide
- lint
- formatter
- dependency management
- package
- versioning
- semantic versioning
- breaking change
- deprecation
- migration

## 这一部分会非常贴近每天写代码和参与 GitHub 工作流。

# Part 6：Open Source / Git / Engineering Culture（开源、Git、代码协作文化）

这一部分和前面几部分有一点不同。

前面：

- Part 1：管理事情
- Part 2：设计系统
- Part 3：交付软件
- Part 4：保证稳定
- Part 5：团队沟通

而这一部分：

> **描述工程师如何共同维护代码资产。**

尤其在：

- GitHub
- GitLab
- 开源项目
- 大型公司研发流程

里面，这些词几乎每天都会出现。

---

# 1. Repository（仓库）

很多人直接翻译：

仓库。

但是工程文化里的 repository 不只是一个文件夹。

---

## Repository

> A place where source code, history, configuration, and collaboration happen.

代码 + 历史 + 协作的地方。

例如：

一个 Git repository 包含：

```text
project/

├── source code

├── commit history

├── branches

├── tags

├── documentation

└── configuration
```

---

所以：

GitHub repo

不是：

“代码文件夹”。

而是：

“一个项目的协作空间”。

---

常见：

> Clone the repository.

克隆项目。

---

> The repository contains the backend service.

这个仓库包含后端服务。

---

# 2. Source Code（源代码）

基础词。

---

## Source

来源。

Source code：

人写的代码。

对应：

Machine code：

机器执行的代码。

---

关系：

```text
Source Code

↓

Compiler

↓

Executable Binary
```

---

# 3. Version Control（版本控制）

Git 的核心。

---

## Version Control System (VCS)

管理：

- code changes
- history
- collaboration

---

Git：

就是一种 VCS。

---

为什么需要？

因为代码不是一次写完。

需要知道：

- 谁改的
- 为什么改
- 怎么恢复

---

# 4. Git

很多人只把 Git 当工具。

但是工程文化里：

Git 是：

> A collaboration model.

---

Git 提供：

- commit
- branch
- merge
- history
- review

---

# 5. Commit（提交）

这是 Git 最重要的概念。

---

很多中文理解：

commit = 保存。

不准确。

---

Commit：

> A meaningful snapshot of changes.

一个有意义的修改记录。

---

好的 commit：

```text
Add retry logic for payment API
```

坏：

```text
update code
```

---

为什么重要？

因为 commit 是：

- review 单位
- rollback 单位
- history 单位

---

常见：

> Please make a separate commit for this change.

---

# 6. Commit Message（提交信息）

工程文化很重视。

---

目的：

未来的人看历史。

---

好的：

```text
Fix timeout issue in payment service
```

---

差：

```text
fix
```

---

# 7. Branch（分支）

很多新人理解：

复制一份代码。

不完全。

---

Branch：

> An independent line of development.

独立开发路线。

---

例如：

```text
main

 |

 +-- feature/login

 +-- feature/payment

 +-- bugfix/api-error
```

---

目的：

隔离变化。

---

# 8. Main / Master Branch

主分支。

---

代表：

稳定代码。

现在大多数项目使用：

main。

---

常见：

> Merge into main branch.

---

# 9. Feature Branch（功能分支）

开发新功能。

例如：

```text
feature/add-payment
```

---

流程：

```text
Create branch

↓

Develop

↓

Review

↓

Merge
```

---

# 10. Bugfix Branch

修 bug。

例如：

```text
bugfix/login-error
```

---

# 11. Release Branch

发布准备分支。

---

用于：

- testing
- stabilization

---

例如：

```text
release/v2.0
```

---

# 12. Hotfix Branch

生产紧急修复。

---

例如：

```text
hotfix/payment-crash
```

---

# 13. Merge（合并）

把两个开发历史合起来。

---

例如：

```text
feature branch

↓

merge

↓

main
```

---

常见：

> Merge this pull request.

---

# 14. Merge Conflict（合并冲突）

非常常见。

---

发生：

两个修改碰到了同一个地方。

例如：

Alice：

```python
timeout = 30
```

Bob：

```python
timeout = 60
```

Git 不知道选择哪个。

---

表达：

> Resolve the merge conflict.

---

# 15. Pull Request (PR)

现代工程文化核心。

---

不是：

“拉请求”。

---

Pull Request：

> A request to merge code changes into another branch.

---

流程：

```text
Developer

↓

Push branch

↓

Create PR

↓

Review

↓

Approve

↓

Merge
```

---

PR 包含：

- code change
- discussion
- review history

---

# 16. Merge Request (MR)

GitLab 使用。

概念和 PR 一样。

---

区别：

GitHub：

Pull Request

GitLab：

Merge Request

---

# 17. Code Review

前面提过。

这里看 Git 文化。

---

Code Review 不是：

找错误。

主要：

- quality
- maintainability
- knowledge sharing

---

好的 review：

> This approach might introduce unnecessary coupling.

不是：

> Your code is wrong.

---

# 18. Reviewer（审核者）

---

负责：

检查代码。

---

常见：

> Add a reviewer to the PR.

---

# 19. Approver（批准者）

---

拥有批准权限。

---

例如：

某些代码：

必须：

- 2 approvals

---

# 20. Maintainer（维护者）

开源文化非常重要。

---

Maintainer：

负责：

- project direction
- accepting contributions
- releases

---

例如：

Linux maintainer。

---

# 21. Contributor（贡献者）

---

任何贡献代码的人。

包括：

- employees
- external developers

---

区别：

Contributor：

贡献过。

Maintainer：

维护项目。

---

# 22. Fork（派生）

开源高频。

---

Fork：

复制一个仓库到自己的账号。

---

例如：

```text
Original Repo

        ↓

Your Fork
```

---

用途：

修改后提交 PR。

---

# 23. Upstream（上游）

开源非常重要。

---

假设：

你 fork：

```text
Your Repo

        ↓

Original Project
```

原项目：

upstream。

---

常见：

> Sync with upstream.

---

# 24. Downstream（下游）

相反。

---

依赖你的项目。

---

例如：

Library：

↓

Application

Library 是 upstream。

Application 是 downstream。

---

# 25. Clone（克隆）

复制仓库到本地。

---

```bash
git clone
```

---

不是：

复制文件。

复制：

代码 + 历史。

---

# 26. Pull（拉取）

获取远程更新。

---

例如：

```bash
git pull
```

---

意思：

同步。

---

# 27. Push（推送）

发送本地提交到远程。

---

```bash
git push
```

---

# 28. Fetch（获取）

容易和 pull 混。

---

Fetch：

下载更新。

但是：

不自动合并。

---

Pull：

fetch + merge。

---

# 29. Rebase（变基）

很多新人难理解。

---

目的：

整理 commit history。

---

例如：

原：

```text
A---B---C

     \
      D---E
```

rebase：

```text
A---B---C---D'---E'
```

---

让历史更线性。

---

表达：

> Rebase your branch before merging.

---

# 30. Cherry-pick（挑选提交）

非常工程化。

---

意思：

拿某一个 commit。

---

例如：

main：

有 bug fix。

release branch：

也需要。

不用 merge 全部。

直接：

```bash
git cherry-pick abc123
```

---

表达：

> Cherry-pick the fix into the release branch.

---

# 31. Tag（标签）

版本标记。

---

例如：

```text
v1.0.0
v2.0.0
```

---

用途：

release。

---

# 32. Release（版本发布）

GitHub release：

通常关联：

- tag
- binary
- notes

---

例如：

> Create a release for v2.0.

---

# 33. Semantic Versioning（语义化版本）

简称：

SemVer。

格式：

```text
MAJOR.MINOR.PATCH
```

例如：

```text
2.5.3
```

---

# 34. Major Version

大版本。

表示：

breaking changes。

例如：

```text
1.x

↓

2.x
```

---

# 35. Minor Version

增加功能。

通常：

兼容。

例如：

```text
2.1

↓

2.2
```

---

# 36. Patch Version

修复。

例如：

```text
2.2.1

↓

2.2.2
```

---

# 37. Breaking Change

再次出现。

Git 文化里非常重要。

---

例如：

API：

旧：

```json
{
  "name": "Tom"
}
```

新：

```json
{
  "userName": "Tom"
}
```

旧客户端坏。

---

# 38. Deprecation（弃用）

非常常见。

---

不是删除。

而是：

> Still available but no longer recommended.

---

例如：

API：

```text
v1 deprecated
v2 recommended
```

---

表达：

> This method is deprecated.

---

# 39. Migration（迁移）

大型工程高频。

---

从旧系统：

↓

新系统。

---

例如：

Database migration。

---

注意：

Migration 不只是搬数据。

包括：

- schema change
- code update
- compatibility

---

# 40. Backward Compatibility

Git / API 文化重要。

---

意思：

新版本支持旧用户。

---

例如：

Library update:

旧代码仍然运行。

---

# 41. Convention（约定）

工程文化非常重要。

---

意思：

团队共同遵守的规则。

---

例如：

Naming convention。

---

表达：

> Follow the coding convention.

---

# 42. Coding Style（代码风格）

---

例如：

- indentation
- naming
- formatting

---

目的：

统一。

---

# 43. Style Guide（规范）

比 convention 更正式。

---

例如：

Google Java Style Guide。

---

# 44. Linter（代码检查工具）

自动发现：

- style issue
- possible bug

---

例如：

ESLint。

---

表达：

> The linter detected an issue.

---

# 45. Formatter（格式化工具）

自动格式代码。

例如：

- Prettier
- gofmt

---

区别：

Linter：

检查。

Formatter：

修改格式。

---

# 46. Static Analysis（静态分析）

不运行代码分析。

---

检查：

- bugs
- security issues

---

# 47. Dependency Management（依赖管理）

现代开发核心。

---

项目依赖：

```text
Application

↓

Libraries

↓

Packages
```

---

需要管理：

- version
- security
- compatibility

---

# 48. Package（包）

软件组成单位。

---

例如：

npm package

Python package

---

# 49. Package Manager

管理 package。

例如：

- npm
- pip
- Maven

---

# 50. Dependency Version Conflict

常见问题。

---

例如：

A 要：

```text
library v1
```

B 要：

```text
library v2
```

---

冲突。

---

# 51. Lock File

例如：

```text
package-lock.json
poetry.lock
```

---

作用：

固定依赖版本。

---

# 52. Build Artifact

Part 3 提过。

这里从 Git 看：

commit：

↓

build：

↓

artifact

---

# 53. Clean Build

重新从零构建。

---

用于：

避免缓存问题。

---

# 54. Reproducible Build（可重复构建）

高级工程概念。

---

意思：

同样源码：

应该产生同样结果。

---

# 55. Monorepo（单仓库）

多个项目放一个 repo。

例如：

Google 风格。

---

# 56. Multi-repo（多仓库）

一个项目一个 repo。

---

区别：

|          | Monorepo | Multi-repo |
| -------- | -------- | ---------- |
| 集中程度 | 高       | 低         |

---

# 57. Code Ownership（代码所有权）

非常重要。

---

例如：

CODEOWNERS 文件。

定义：

哪个团队负责哪些代码。

---

# 58. Contribution Guideline

开源常见。

---

告诉别人：

如何贡献。

包括：

- coding style
- PR process

---

# 59. Changelog（变更日志）

记录：

版本变化。

---

例如：

```text
v2.1.0

Added:
- New API

Fixed:
- Login issue
```

---

# 60. Documentation（文档）

工程资产。

包括：

- README
- API docs
- Design docs

---

# 这一部分总结：工程师如何看待代码

成熟工程团队认为：

代码不是文件。

而是：

```text
Code

↓

Repository

↓

History

↓

Review

↓

Collaboration

↓

Release

↓

Maintenance
```

---

所以他们说：

普通：

> 我改了一些代码。

工程：

> I pushed a commit and opened a PR. The reviewer requested changes, so I rebased the branch and updated the implementation.

普通：

> 发布新版。

工程：

> We tagged v2.1.0, generated the release artifact, and rolled it out gradually.

---

# 到这里，6 个 Part 的整体地图已经形成

```text
Software Engineering Language

        |
        |
        +-- Workflow
        |
        +-- Architecture
        |
        +-- Delivery
        |
        +-- Reliability
        |
        +-- Communication
        |
        +-- Git / Open Source
```

你现在看到的其实已经接近一个国外软件团队内部使用的“概念词库”。

下一步如果继续深入，我建议不是继续堆词，而是做两个方向：

1. **把这些词整理成「中文思维 → 英文工程表达」转换表**

例如：

> “没人负责”
>
> ❌ Nobody is responsible
>
> ✅ There is no clear ownership.

---

2. **模拟真实工程场景**

例如：

- Jira 写 issue
- Slack 讨论 bug
- Code Review 评论
- Design Doc 写法
- Incident Postmortem 写法

## 因为真正掌握这些词，需要看到它们在句子里的位置。你现在已经有“词汇地图”，下一步应该练“工程语言输出”。

好的，继续补全。

前面 Part 1-6 主要解决的是：

> **软件团队如何协作、管理、交付和维护系统**

Part 7-11 会进入：

> **工程师讨论代码、系统、数据库、云、安全时真正使用的技术语言**

这部分更接近“技术设计会议”和“代码讨论”。

---

# Part 7：Programming Language & Code Level Vocabulary（编程语言与代码层词汇）

这一部分是工程师每天写代码、Review 代码时使用的语言。

核心思想：

代码不是一堆语句，而是：

```text
Data（数据）

↓

Logic（逻辑）

↓

State（状态）

↓

Behavior（行为）
```

---

# 1. Variable（变量）

最基础。

---

## 含义

存储数据的名字。

例如：

```python
user_name = "Tom"
```

user_name：

variable。

---

常见表达：

> Rename this variable.

重命名变量。

---

# 2. Constant（常量）

不会改变的值。

例如：

```python
MAX_RETRY = 3
```

---

区别：

Variable:

可以变。

Constant:

固定。

---

# 3. Value（值）

变量里面存的东西。

例如：

```python
age = 20
```

age：

variable

20：

value

---

# 4. Type（类型）

数据类型。

例如：

- string
- integer
- boolean
- object

---

表达：

> Type mismatch occurred.

类型不匹配。

---

# 5. Function（函数）

代码行为的基本单位。

---

Function：

输入：

↓

处理

↓

输出

例如：

```python
calculate_price()
```

---

# 6. Method（方法）

属于对象的 function。

例如：

```python
user.login()
```

login：

method

---

区别：

Function：

独立。

Method：

属于 object。

---

# 7. Parameter（参数）

函数定义里的变量。

例如：

```python
def login(username):
```

username：

parameter

---

# 8. Argument（实参）

调用时传入的值。

例如：

```python
login("Tom")
```

"Tom":

argument

---

关系：

```text
Parameter

↓

Argument
```

---

# 9. Return Value（返回值）

函数输出。

例如：

```python
result = calculate()
```

result：

return value

---

# 10. Exception（异常）

程序运行中的异常情况。

例如：

- network error
- invalid input

---

表达：

> Handle exceptions properly.

---

# 11. Error Handling（错误处理）

处理异常的机制。

包括：

- retry
- fallback
- logging

---

# 12. State（状态）

非常重要。

---

State：

系统当前情况。

例如：

订单：

```text
CREATED

↓

PAID

↓

SHIPPED

↓

COMPLETED
```

这些都是 state。

---

# 13. Stateful / Stateless

非常常见。

---

## Stateful

保存状态。

例如：

服务器保存 session。

---

## Stateless

不保存状态。

例如：

REST API。

---

# 14. Side Effect（副作用）

高级工程词。

---

函数除了返回值，还改变外部东西。

例如：

```python
save_user()
```

改变数据库。

这是 side effect。

---

# 15. Pure Function（纯函数）

没有副作用。

输入：

↓

输出

相同输入：

永远相同结果。

---

# 16. Mutable / Immutable（可变 / 不可变）

非常常见。

---

Mutable：

可以修改。

例如：

list

Immutable：

不能修改。

例如：

string（很多语言）

---

# 17. Object（对象）

面向对象基础。

---

包含：

- data
- behavior

---

# 18. Class（类）

对象模板。

---

例如：

```python
class User:
```

---

# 19. Instance（实例）

类创建出来的对象。

---

Class:

设计图。

Instance:

实际对象。

---

# 20. Interface（接口）

非常重要。

---

不是 API 才叫 interface。

Interface：

定义行为约束。

例如：

```java
interface Payment
```

---

# 21. Implementation（实现）

接口具体怎么做。

---

例如：

Interface：

```text
Payment
```

Implementation：

```text
StripePayment
PaypalPayment
```

---

# 22. Abstraction（抽象）

工程核心思想。

---

隐藏细节，只暴露重要部分。

例如：

你调用：

```python
send_email()
```

不用知道 SMTP 细节。

---

# 23. Encapsulation（封装）

隐藏内部状态。

---

目的：

降低耦合。

---

# 24. Inheritance（继承）

类之间复用。

---

现在很多工程更偏向：

Composition。

---

# 25. Composition（组合）

通过组合对象实现功能。

---

经典：

> Prefer composition over inheritance.

---

# 26. Dependency（依赖）

代码层也有。

---

例如：

A 使用 B。

A depends on B。

---

# 27. Coupling（耦合）

两个模块关联程度。

---

高：

high coupling

低：

low coupling

---

目标：

减少 coupling。

---

# 28. Cohesion（内聚）

模块内部相关程度。

---

目标：

high cohesion。

---

经典：

```text
Good Design:

Low Coupling

+

High Cohesion
```

---

# 29. Refactoring（重构）

改变代码结构。

不改变行为。

---

例如：

优化：

- readability
- maintainability

---

# 30. Technical Debt（技术债）

非常重要。

---

为了速度留下的问题。

例如：

快速写 hack。

未来需要偿还。

---

表达：

> We need to pay down technical debt.

---

# Part 7 核心模型

```text
Code

↓

Function

↓

Object

↓

Module

↓

Architecture
```

---

---

# Part 8：Backend & Distributed System Vocabulary（后端与分布式系统）

这是大型互联网系统核心。

---

# 1. Client（客户端）

发请求的一方。

例如：

Browser

Mobile App

---

# 2. Server（服务器）

处理请求。

---

# 3. Request（请求）

客户端发送。

---

# 4. Response（响应）

服务器返回。

---

关系：

```text
Client

request →

Server

response →

Client
```

---

# 5. Endpoint（接口端点）

API 地址。

例如：

```text
GET /users
```

---

# 6. API（Application Programming Interface）

系统之间通信方式。

---

# 7. REST API

基于 HTTP 的 API 风格。

---

# 8. Authentication（认证）

你是谁？

---

例如：

登录。

---

# 9. Authorization（授权）

你能做什么？

---

区别：

Authentication:

身份。

Authorization:

权限。

---

# 10. Session（会话）

用户状态。

---

# 11. Token

身份凭证。

例如：

JWT。

---

# 12. Middleware（中间件）

请求处理链中的组件。

例如：

Authentication middleware。

---

# 13. Service（服务）

独立业务组件。

---

# 14. Microservice（微服务）

小型独立服务。

---

# 15. Monolith（单体）

一个大应用。

---

# 16. Queue（队列）

异步处理。

---

例如：

订单：

提交任务：

↓

Queue

↓

Worker

---

# 17. Message Broker

消息中间件。

例如：

Kafka。

---

# 18. Event（事件）

系统发生的事情。

例如：

OrderCreated。

---

# 19. Event-driven Architecture

事件驱动架构。

---

# 20. Cache（缓存）

减少访问成本。

---

例如：

Redis。

---

# 21. Hit / Miss

缓存命中 / 未命中。

---

# 22. Load Balancer（负载均衡）

分配流量。

---

# 23. Gateway（网关）

统一入口。

---

# 24. Transaction（事务）

一组操作必须一起成功。

---

# 25. Consistency（一致性）

数据保持一致。

---

# 26. Availability（可用性）

系统可访问。

---

# 27. Partition（分区）

分布式数据拆分。

---

# 28. Replication（复制）

数据复制。

---

# 29. Eventual Consistency（最终一致性）

分布式经典概念。

---

# 30. CAP Theorem

分布式理论：

Consistency

Availability

Partition tolerance

---

# Part 8 核心模型

```text
Request

↓

Service

↓

Database

↓

Response
```

大型系统：

```text
Client

↓

Gateway

↓

Services

↓

Queue

↓

Database
```

---

（由于单条消息长度限制，我继续发送 Part 9-11。）

下一条继续：

# Part 9：Database Vocabulary

# Part 10：Cloud / DevOps Vocabulary

# Part 11：Security Vocabulary

这三部分会补齐：

- SQL
- 数据建模
- Kubernetes
- Docker
- Cloud
- IAM
- Encryption
- Vulnerability
- Threat Model

## 也是实际工作中非常高频的一批。

继续补齐 Part 9-11。

到这里，前面的 Part 1-8 已经覆盖：

- 工程协作语言
- 系统设计语言
- 软件交付语言
- SRE 稳定性语言
- Git/代码协作语言
- 编程语言基础
- 后端系统语言

这三个 Part 是：

- **Part 9：Database Vocabulary（数据库语言）**
- **Part 10：Cloud / DevOps Vocabulary（云计算与基础设施语言）**
- **Part 11：Security Vocabulary（安全工程语言）**

这三块基本就是后端工程师、架构师、SRE 日常讨论的核心词汇。

---

# Part 9：Database Vocabulary（数据库领域词汇）

数据库相关英语有一个特点：

很多词不是技术名词，而是描述**数据生命周期**。

核心模型：

```text
Data

↓

Storage

↓

Query

↓

Transaction

↓

Consistency

↓

Optimization
```

---

# 1. Database（数据库）

基础。

但是工程里通常区分：

---

## Database

整个数据库系统。

例如：

MySQL database。

---

## Data Store

更广。

可以包括：

- database
- cache
- object storage

---

# 2. Table（表）

关系数据库核心。

例如：

```sql
users

id | name | email
```

---

# 3. Row（行）

一条记录。

例如：

```text
1 | Tom | tom@example.com
```

---

# 4. Column（列）

字段。

例如：

```text
id

name

email
```

---

# 5. Schema（模式）

非常重要。

Schema：

> The structure that defines how data is organized.

包括：

- tables
- columns
- relationships
- constraints

---

例如：

```text
User Schema

users table

orders table

payments table
```

---

# 6. Data Model（数据模型）

描述：

数据如何组织。

常见：

- relational model
- document model
- graph model

---

# 7. Entity（实体）

数据库设计常见。

例如：

业务对象：

- User
- Order
- Product

---

# 8. Relationship（关系）

实体之间关系。

例如：

```text
User

has many

Orders
```

---

# 9. Primary Key（主键）

唯一标识一条记录。

例如：

```text
user_id
```

---

# 10. Foreign Key（外键）

关联其他表。

例如：

```text
orders.user_id

↓

users.id
```

---

# 11. Index（索引）

数据库性能核心。

---

作用：

加快查询。

没有 index：

扫描全部数据。

有 index：

快速定位。

---

表达：

> Add an index to improve query performance.

---

# 12. Query（查询）

读取数据。

---

例如：

SQL query。

---

# 13. Query Optimization（查询优化）

提高查询效率。

包括：

- index
- execution plan
- query rewrite

---

# 14. Execution Plan（执行计划）

数据库如何执行 SQL。

---

例如：

是否：

- full table scan
- index lookup

---

# 15. Full Table Scan（全表扫描）

性能问题常见。

---

意思：

扫描整张表。

---

# 16. Migration（数据库迁移）

非常高频。

---

改变数据库结构。

例如：

增加字段：

```sql
ALTER TABLE users ADD COLUMN age INT;
```

---

# 17. Migration Script（迁移脚本）

执行 schema change 的代码。

---

# 18. Backfill（数据回填）

大型系统常见。

---

已有数据：

补充新字段。

例如：

新增：

```text
created_at
```

给历史数据填充。

---

# 19. Transaction（事务）

数据库核心。

---

多个操作：

要么全部成功：

要么全部失败。

---

例如：

转账：

```text
A -100

B +100
```

不能只执行一半。

---

# 20. ACID

数据库事务原则。

---

## Atomicity

原子性。

全部成功或全部失败。

---

## Consistency

一致性。

数据满足规则。

---

## Isolation

隔离性。

并发操作互不干扰。

---

## Durability

持久性。

提交后不会丢。

---

# 21. Isolation Level（隔离级别）

控制并发行为。

例如：

- Read Committed
- Repeatable Read
- Serializable

---

# 22. Deadlock（死锁）

数据库常见问题。

---

两个事务互相等待。

---

表达：

> The transaction was blocked due to a deadlock.

---

# 23. Lock（锁）

控制并发访问。

---

例如：

row lock。

---

# 24. Replication（复制）

数据复制。

---

例如：

Primary:

写

Replica:

读

---

# 25. Primary / Replica

数据库架构常见。

---

以前：

Master / Slave

现在更多：

Primary / Replica

---

# 26. Sharding（分片）

水平拆分数据。

---

例如：

用户数据：

Shard A

Shard B

---

# 27. Partitioning（分区）

把数据分成部分。

---

区别：

Sharding：

多个数据库节点。

Partitioning：

一个数据库内部。

---

# 28. Normalization（规范化）

减少数据重复。

---

例如：

用户信息不要复制到每张表。

---

# 29. Denormalization（反规范化）

为了性能主动重复数据。

---

例如：

保存冗余字段减少 join。

---

# 30. Join（连接）

关联多个表。

---

例如：

User + Order。

---

# 31. Stored Procedure（存储过程）

数据库内部代码。

---

现在很多现代系统减少使用。

---

# 32. Database Constraint（约束）

保证数据正确。

例如：

- NOT NULL
- UNIQUE
- CHECK

---

# 33. Data Integrity（数据完整性）

数据保持正确。

---

# 34. Backup（备份）

保存副本。

---

# 35. Restore（恢复）

从备份恢复。

---

# 36. Point-in-time Recovery（时间点恢复）

恢复到某个时间。

---

# 37. Database Failover

数据库故障切换。

---

# Part 9 总结

数据库工程思维：

```text
Design Schema

↓

Store Data

↓

Query Data

↓

Optimize Performance

↓

Maintain Consistency
```

---

---

# Part 10：Cloud / DevOps Vocabulary（云计算与 DevOps）

现代工程团队非常重要。

核心模型：

```text
Application

↓

Container

↓

Infrastructure

↓

Cloud Platform

↓

Automation
```

---

# 1. Infrastructure（基础设施）

包括：

- servers
- network
- storage

---

# 2. Infrastructure as Code (IaC)

非常重要。

---

用代码管理基础设施。

例如：

Terraform。

---

表达：

> Infrastructure should be managed as code.

---

# 3. Server（服务器）

运行程序的机器。

---

# 4. Virtual Machine (VM)

虚拟机。

---

一台物理机器：

↓

多个虚拟机器。

---

# 5. Container（容器）

比 VM 更轻。

---

例如：

Docker。

---

# 6. Docker Image

镜像。

包含：

- application
- dependencies
- runtime

---

# 7. Docker Container

运行中的 image。

---

关系：

```text
Image

↓

Container
```

---

# 8. Dockerfile

定义如何构建 image。

---

# 9. Registry

存储 image 的地方。

例如：

Docker Registry。

---

# 10. Kubernetes (K8s)

容器编排平台。

---

负责：

- deployment
- scaling
- networking

---

# 11. Pod

Kubernetes 最小运行单位。

---

# 12. Cluster

一组机器组成的 Kubernetes 环境。

---

# 13. Node

Cluster 中的一台机器。

---

# 14. Deployment

管理应用部署。

---

# 15. Service（Kubernetes）

网络访问入口。

---

注意：

这里 Service 不一定是业务服务。

---

# 16. Namespace

资源隔离。

---

# 17. Ingress

外部访问入口。

---

# 18. Load Balancing

流量分配。

---

# 19. Auto Scaling

自动扩容。

---

例如：

流量增加：

服务器数量增加。

---

# 20. Horizontal Scaling

增加机器数量。

---

# 21. Vertical Scaling

增加机器能力。

---

# 22. Configuration Management

配置管理。

---

例如：

环境变量。

---

# 23. Secret Management

管理敏感信息。

例如：

密码。

API Key。

---

# 24. Environment Variable

环境变量。

---

例如：

```text
DATABASE_URL
API_KEY
```

---

# 25. CI/CD Pipeline

之前讲过。

这里看 DevOps。

---

自动：

- build
- test
- deploy

---

# 26. Infrastructure Monitoring

基础设施监控。

例如：

CPU

Memory

Network

---

# 27. Provisioning

创建资源。

例如：

创建服务器。

---

# 28. Deprovisioning

释放资源。

---

# 29. Region

云区域。

例如：

Tokyo Region。

---

# 30. Availability Zone

可用区。

---

提高：

fault tolerance。

---

# 31. Serverless

无需管理服务器。

---

例如：

Function as a Service。

---

# 32. Managed Service

云厂商托管服务。

例如：

Managed Database。

---

# 33. Cloud-native

云原生。

特点：

- container
- automation
- scalability

---

# 34. Immutable Infrastructure

不可变基础设施。

---

不修改旧服务器。

而是：

重新创建。

---

# 35. Deployment Strategy

部署策略。

包括：

- blue-green
- canary
- rolling update

---

# Part 10 总结

DevOps 思维：

```text
Code

↓

Build

↓

Package

↓

Deploy

↓

Operate

↓

Monitor
```

---

---

# Part 11：Security Vocabulary（安全工程语言）

安全领域词汇非常重要。

核心：

```text
Protect

↓

Detect

↓

Respond

↓

Recover
```

---

# 1. Security（安全）

大概念。

---

包括：

- application security
- infrastructure security
- data security

---

# 2. Vulnerability（漏洞）

系统弱点。

---

例如：

SQL injection。

---

# 3. Exploit（利用）

利用漏洞攻击。

---

区别：

Vulnerability：

漏洞。

Exploit：

利用方式。

---

# 4. Threat（威胁）

潜在危险。

---

# 5. Threat Model（威胁模型）

安全设计核心。

---

分析：

- 谁攻击？
- 怎么攻击？
- 如何防御？

---

# 6. Attack Surface（攻击面）

系统可能被攻击的位置。

---

例如：

- API
- login page
- database

---

# 7. Authentication（认证）

再次出现。

确认身份。

---

# 8. Authorization（授权）

确认权限。

---

# 9. Access Control（访问控制）

管理：

谁可以访问什么。

---

# 10. Permission（权限）

具体允许做什么。

---

# 11. Role（角色）

权限集合。

例如：

Admin

User

---

# 12. Principle of Least Privilege（最小权限原则）

安全核心。

---

用户只拥有必要权限。

---

# 13. Encryption（加密）

保护数据。

---

# 14. Encryption at Rest

静态数据加密。

例如：

数据库。

---

# 15. Encryption in Transit

传输加密。

例如：

HTTPS。

---

# 16. Hashing（哈希）

不可逆转换。

例如：

密码存储。

---

# 17. Salt（盐）

增加密码哈希安全性。

---

# 18. Secret（密钥/秘密信息）

例如：

API key。

---

# 19. Credential（凭证）

身份验证信息。

---

例如：

username/password/token。

---

# 20. Certificate（证书）

用于证明身份。

---

例如：

TLS certificate。

---

# 21. TLS / SSL

通信加密协议。

---

# 22. Firewall（防火墙）

控制网络访问。

---

# 23. Network Security Group

云环境访问控制。

---

# 24. Security Patch

安全补丁。

---

# 25. CVE

漏洞编号。

---

例如：

CVE-2025-xxxx

---

# 26. Penetration Testing（渗透测试）

模拟攻击。

---

# 27. Security Audit（安全审计）

检查安全状态。

---

# 28. Compliance（合规）

满足规则。

例如：

GDPR。

---

# 29. Data Privacy（数据隐私）

保护用户数据。

---

# 30. Incident Response（安全事件响应）

安全事故处理。

---

例如：

数据泄露。

---

# 31. Breach（泄露）

安全事件。

---

例如：

Data breach。

---

# 32. Malware（恶意软件）

恶意程序。

---

# 33. Phishing（钓鱼攻击）

欺骗获取信息。

---

# 34. Injection Attack

注入攻击。

例如：

SQL injection。

---

# 35. XSS

跨站脚本攻击。

---

# 36. CSRF

跨站请求伪造。

---

# 37. Rate Limiting（限流）

防止滥用。

---

# 38. DDoS

分布式拒绝服务攻击。

---

# 39. Security Review

安全评审。

---

# 40. Secure by Design

安全设计理念。

---

# Part 11 总结

安全工程思维：

```text
Identify Risk

↓

Prevent Attack

↓

Detect Incident

↓

Respond Quickly

↓

Improve Security
```

---

# 到这里，Part 1-11 完整体系：

```text
Software Engineering English

1. Workflow & Issue Management
2. Architecture & System Design
3. Development Lifecycle & Delivery
4. SRE & Reliability
5. Engineering Communication
6. Git & Open Source
7. Programming & Code
8. Backend & Distributed System
9. Database
10. Cloud & DevOps
11. Security
```

这 11 个模块已经覆盖了一个中高级软件工程师在国际团队中 **90%左右的日常技术沟通词汇体系**。

下一步最值得做的不是继续扩词，而是进入**“英语输出训练”**：

例如：

中文：

> “这个需求没有明确负责人，而且进度不可见，导致大家反复沟通。”

训练成：

> "There is unclear ownership for this request, and the lack of visibility makes it difficult to track progress."

也就是建立：

**中文概念 → 工程场景 → 英语表达**

## 这个转换能力，才是真正摆脱中文中转的关键。

这个问题问得非常关键。

前面 11 个 Part 确实大量是**名词（concept nouns）**，因为软件工程文化最先需要建立的是“概念地图”。

但是实际工程英语里，**真正让表达像工程师的，往往是动词**。

很多中文开发者的问题不是不知道名词，而是：

知道：

- issue
- ownership
- dependency
- deployment
- architecture

但是不会说：

- 谁对它做什么？
- 事情现在处于什么动作状态？

例如：

中文：

> 我们需要解决这个问题。

很多人：

> We need to solve this problem.

没错，但工程团队更常：

> We need to address this issue.

或者：

> We need to investigate this issue first.

这里区别就在动词。

---

# 先说结论

## 1. 有一部分动词就是普通英语

比如：

- add
- remove
- change
- create
- update
- fix
- check
- test

这些不用特殊积累。

---

## 2. 但是工程领域有大量“固定搭配动词”

这些不是普通英语思维能推出来的。

比如：

中文：

> 提出一个问题

普通：

> say a problem

工程：

> raise an issue

---

中文：

> 处理一个问题

普通：

> deal with a problem

工程：

> address an issue

---

中文：

> 引入一个依赖

普通：

> add a dependency

工程：

> introduce a dependency

---

中文：

> 删除旧 API

普通：

> remove old API

工程：

> deprecate an API

---

所以需要积累的是：

> **Engineering Verb + Object 搭配**

不是单独背动词。

---

# 软件工程最常用动词分类

---

# 1. 创建类（Create）

## create

最普通。

> Create a new service.

---

## add

增加东西。

> Add a new endpoint.

---

## introduce

引入新概念、新机制。

这个非常工程。

例如：

> Introduce a caching layer.

意思：

引入缓存层。

---

## implement

实现。

这是工程最重要动词之一。

例如：

> Implement the authentication flow.

注意：

不是：

write code。

implement 更偏：

把设计变成实际功能。

---

## build

构建。

例如：

> Build a scalable system.

---

## generate

生成。

例如：

> Generate a report.

> Generate a build artifact.

---

# 2. 修改类（Change）

---

## update

更新。

最万能。

> Update the configuration.

---

## modify

修改。

比 update 更偏：

改变已有东西。

> Modify the existing behavior.

---

## change

普通改变。

---

## refactor

重构。

非常工程。

> Refactor the payment module.

---

## migrate

迁移。

非常重要。

> Migrate the database to PostgreSQL.

---

## optimize

优化。

> Optimize query performance.

---

## improve

改善。

> Improve system reliability.

---

# 3. 删除类（Remove）

---

## remove

删除。

> Remove unused code.

---

## delete

真正删除。

> Delete old records.

---

## deprecate

弃用。

这是工程中特有。

例如：

> Deprecate the old API.

意思：

不推荐继续使用，但可能暂时保留。

---

## retire

淘汰。

更偏系统生命周期。

> Retire the legacy service.

---

# 4. 修复类（Fix）

---

## fix

修 bug。

> Fix the login issue.

---

## resolve

解决。

比 fix 更正式。

> Resolve the incident.

---

## address

处理。

工程高频。

重点：

不一定完全解决。

例如：

> Address performance concerns.

---

## mitigate

缓解。

特别用于风险、事故。

> Mitigate the impact.

---

## prevent

防止。

> Prevent future failures.

---

## avoid

避免。

> Avoid unnecessary complexity.

---

# 5. 分析类（Understand）

这批非常重要。

---

## analyze

分析数据。

> Analyze performance metrics.

---

## investigate

调查问题。

线上事故高频。

> Investigate the root cause.

---

## identify

识别。

> Identify potential risks.

---

## detect

检测。

系统自动发现。

> Detect anomalies.

---

## trace

追踪。

> Trace the request flow.

---

## monitor

监控。

> Monitor system health.

---

## observe

观察。

> Observe user behavior.

---

# 6. 设计类（Design）

---

## design

设计。

> Design an API.

---

## define

定义。

非常常见。

例如：

> Define the interface contract.

---

## specify

规定详细规格。

例如：

> Specify API behavior.

---

## architect

设计架构。

高级表达。

> Architect a distributed system.

---

## structure

组织结构。

> Structure the code properly.

---

# 7. 讨论决策类

这部分和 Part 5 强相关。

---

## discuss

讨论。

---

## review

评审。

工程超级高频。

> Review the proposal.

---

## evaluate

评估。

> Evaluate different approaches.

---

## consider

考虑。

> Consider another solution.

---

## compare

比较。

---

## choose

选择。

---

## decide

决定。

---

## determine

确定。

区别：

decide：

做决定。

determine：

分析后确定。

例如：

> Determine the root cause.

---

## recommend

推荐。

> Recommend an approach.

---

# 8. 责任和流程类

---

## assign

分配。

> Assign the task to Alice.

---

## own

负责。

注意：

这里 own 是动词。

> I own this component.

非常工程。

---

## handle

处理。

> Handle incoming requests.

---

## manage

管理。

> Manage dependencies.

---

## coordinate

协调。

> Coordinate with the backend team.

---

## track

跟踪。

> Track progress.

---

## follow up

跟进。

> Follow up on this issue.

---

## escalate

升级。

> Escalate the problem to the infrastructure team.

---

# 9. 代码变化类

---

## commit

提交代码。

> Commit the changes.

---

## push

推送。

> Push the latest changes.

---

## merge

合并。

> Merge the branch.

---

## rebase

变基。

> Rebase your branch.

---

## cherry-pick

挑 commit。

> Cherry-pick the fix.

---

## review

审核。

> Review the PR.

---

## approve

批准。

> Approve the pull request.

---

# 10. 发布部署类

---

## deploy

部署。

> Deploy the service.

---

## release

发布。

> Release version 2.0.

---

## roll out

逐步发布。

> Roll out the feature gradually.

---

## rollback

回滚。

> Roll back the deployment.

---

## configure

配置。

> Configure the environment.

---

## provision

创建基础设施。

> Provision a new server.

---

## scale

扩容。

> Scale the service horizontally.

---

# 11. 数据库类

---

## query

查询。

> Query the database.

---

## insert

插入。

---

## update

更新。

---

## delete

删除。

---

## migrate

迁移。

---

## replicate

复制。

---

## index

建立索引。

> Index the table.

---

## optimize

优化。

> Optimize the query.

---

## validate

验证。

> Validate the data.

---

# 12. 系统稳定性类

---

## fail

失败。

> The service failed.

---

## recover

恢复。

> Recover from failure.

---

## restart

重启。

---

## retry

重试。

---

## fallback

降级。

> Fall back to cached data.

---

## recover

恢复。

---

## degrade

降级。

> The service degraded under heavy load.

---

# 13. 安全类

---

## authenticate

认证。

> Authenticate the user.

---

## authorize

授权。

> Authorize access.

---

## encrypt

加密。

> Encrypt sensitive data.

---

## decrypt

解密。

---

## validate

验证。

---

## sanitize

清理输入。

例如：

防 SQL injection。

---

## scan

扫描。

> Scan for vulnerabilities.

---

## patch

打补丁。

> Patch the vulnerability.

---

# 一个非常重要的规律：

工程英语喜欢：

## 动词 + 抽象名词

例如：

普通英语：

> fix a bug

工程英语：

> address an issue

---

普通：

> think about the design

工程：

> evaluate the design

---

普通：

> make the system faster

工程：

> optimize system performance

---

普通：

> put a new feature into the system

工程：

> implement a new feature

---

普通：

> remove an old API

工程：

> deprecate an API

---

# 软件工程最常见动词 TOP 30（建议优先背）

如果只选最重要：

| 动词        | 常搭配                 |
| ----------- | ---------------------- |
| implement   | feature, solution      |
| address     | issue, concern         |
| resolve     | problem, incident      |
| investigate | issue, root cause      |
| identify    | risk, problem          |
| define      | requirement, interface |
| design      | system, architecture   |
| review      | code, design, PR       |
| approve     | change, PR             |
| assign      | task, owner            |
| track       | progress, issue        |
| manage      | dependency, resource   |
| coordinate  | team, work             |
| introduce   | feature, dependency    |
| remove      | code, component        |
| deprecate   | API, feature           |
| migrate     | database, system       |
| refactor    | code                   |
| optimize    | performance            |
| configure   | system                 |
| deploy      | service                |
| release     | version                |
| roll out    | feature                |
| rollback    | deployment             |
| monitor     | system                 |
| detect      | issue                  |
| prevent     | failure                |
| mitigate    | impact                 |
| scale       | service                |
| validate    | data, design           |

---

所以回答你的问题：

> “动词使用日常常见的就可以了吗？没有特定场景的动词吧？”

答案：

**基础动作可以用普通动词，但是高级工程表达大量依赖场景化动词。**

而且工程动词比名词更值得练，因为：

名词决定你“懂不懂这个概念”。

动词决定你“像不像在这个团队里工作”。

真正脱离中文中转，需要训练的是：

```
场景
 ↓
工程概念
 ↓
固定动词搭配
 ↓
自然句子
```

比如：

看到：

“上线后发现问题，需要先降低影响，不一定马上修复根因”

脑子应该直接出来：

> We need to mitigate the impact first and investigate the root cause afterward.

## 这就是工程英语思维。

你现在整理到这里，其实已经覆盖了**软件工程英语最核心的“名词 + 动词体系”**。

如果目标是：

> 不经过中文，直接用英语参与国外软件团队的技术沟通

那么前面的 Part 1-11 + 动词体系已经有大约 **80%-90% 的覆盖率**。

不过还有一些“隐藏层”没有展开。这些不是单纯词汇，而是工程师经常使用的**表达模型（expression patterns）**。这些补上之后，会更接近真实工作环境。

我认为还需要补 6 个方向。

---

# Part 12：Engineering Adjectives（工程形容词）

这个非常重要。

很多技术沟通不是：

> 做什么

而是：

> 描述一个东西是什么性质。

工程师大量使用：

---

## 1. scalable（可扩展的）

非常高频。

不是：

“能运行”。

而是：

用户增加以后还能撑住。

例：

> We need a scalable architecture.

---

## 2. maintainable（可维护的）

代码未来容易改。

例如：

> This code is difficult to maintain.

---

## 3. reliable（可靠的）

系统稳定。

---

## 4. resilient（有韧性的）

比 reliable 更高级。

意思：

遇到故障还能恢复。

例如：

> A resilient system can recover from failures.

---

## 5. flexible（灵活的）

容易变化。

---

## 6. extensible（可扩展功能的）

和 scalable 区别：

### scalable

规模扩大。

例如：

100 用户 → 100 万用户。

### extensible

增加能力。

例如：

增加新的支付方式。

---

## 7. compatible（兼容的）

非常常用。

例如：

> Backward compatible.

向后兼容。

---

## 8. reusable（可复用的）

代码设计常用。

---

## 9. modular（模块化的）

---

## 10. loosely coupled（低耦合）

---

## 11. tightly coupled（高耦合）

---

## 12. lightweight（轻量）

例如：

> lightweight service

---

## 13. heavyweight（重量级）

---

## 14. efficient（高效）

---

## 15. optimized（优化过）

---

## 16. robust（健壮）

和 reliable 接近。

robust 更强调：

抗异常情况。

---

## 17. consistent（一致）

---

## 18. deterministic（确定性的）

相同输入：

相同输出。

---

## 19. asynchronous（异步）

---

## 20. synchronous（同步）

---

这些形容词非常重要，因为设计讨论里大量是：

> Is this approach scalable?

> Is this solution maintainable?

> Is this API backward compatible?

---

# Part 13：Engineering Trade-off Vocabulary（工程权衡语言）

这是很多中文开发者缺失的部分。

国外技术讨论非常喜欢谈：

trade-off。

因为工程没有绝对最好。

---

# 1. Trade-off

权衡。

例如：

> There is always a trade-off between performance and simplicity.

---

# 2. Pros and Cons

优缺点。

---

# 3. Advantage / Disadvantage

---

# 4. Benefit / Cost

---

# 5. Complexity

复杂度。

---

# 6. Simplicity

简单性。

---

# 7. Performance

性能。

---

# 8. Maintainability

可维护性。

---

# 9. Scalability

扩展能力。

---

# 10. Reliability

可靠性。

---

工程讨论：

通常不是：

> Which one is better?

而是：

> What are the trade-offs?

---

例如：

方案 A：

性能高，但是复杂。

英文：

> This approach improves performance but increases complexity.

---

方案 B：

简单，但是扩展性差。

> This solution is simpler but less scalable.

---

# Part 14：Requirements & Product Vocabulary（需求和产品沟通）

工程师不仅和工程师交流。

还和：

- Product Manager
- Designer
- Customer

沟通。

---

# 1. Requirement

需求。

---

# 2. Functional Requirement

功能需求。

例如：

用户可以登录。

---

# 3. Non-functional Requirement

非功能需求。

例如：

性能、安全。

---

# 4. User Story

用户故事。

例如：

> As a user, I want to...

---

# 5. Acceptance Criteria

验收标准。

非常 Jira。

---

# 6. Scope

范围。

---

例如：

> This is out of scope.

---

# 7. Priority

优先级。

---

# 8. Constraint

限制条件。

---

# 9. Assumption

假设。

---

# 10. Dependency

依赖。

---

# 11. Milestone

里程碑。

---

# 12. Deadline

截止时间。

---

# 13. Estimate

估算。

---

# 14. Effort

工作量。

---

# 15. Impact

影响。

---

工程讨论：

> What is the impact of this change?

---

# Part 15：Debugging Vocabulary（调试语言）

这个非常实际。

---

# 1. Reproduce

复现。

超级高频。

例如：

> I cannot reproduce the issue.

---

# 2. Reproduction Steps

复现步骤。

---

# 3. Root Cause

根因。

---

# 4. Symptom

症状。

区别：

Bug：

问题。

Symptom：

表现。

---

例如：

用户看到：

页面打不开。

Symptom。

真正原因：

数据库连接失败。

Root cause。

---

# 5. Trace

追踪。

---

# 6. Log

日志。

---

# 7. Stack Trace

堆栈。

---

# 8. Debug

调试。

---

# 9. Inspect

检查。

---

# 10. Isolate

隔离问题。

非常重要。

例如：

> Isolate the issue to the database layer.

---

# 11. Narrow Down

缩小范围。

非常口语化。

---

例如：

> We narrowed down the issue to the cache layer.

---

# 12. Workaround

临时解决方案。

非常重要。

---

区别：

Solution：

正式解决。

Workaround：

绕过去。

---

# 13. Regression

回归问题。

例如：

修 A 导致 B 坏。

---

# 14. Reproduce

再次出现。

---

# Part 16：Engineering Meetings & Communication Phrases（会议表达）

这个可能是最接近真实工作的。

---

## 表达观点

不要：

> I think this is good.

工程：

> I think this approach makes sense.

---

## 提出风险

不要：

> This may have problems.

工程：

> This approach introduces some risks.

---

## 不同意

不要：

> You are wrong.

工程：

> I have some concerns about this approach.

---

## 建议

不要：

> We should change this.

工程：

> I would suggest considering another approach.

---

## 请求解释

不要：

> I don't understand.

工程：

> Could you clarify the reasoning behind this decision?

---

## 推迟决定

工程：

> Let's gather more information before making a decision.

---

# Part 17：Code Review 常用语言

这个非常建议单独掌握。

---

## 1. nit

小问题。

例如：

> Nit: rename this variable.

意思：

不是阻塞问题。

---

## 2. blocker

阻塞问题。

---

## 3. suggestion

建议。

---

## 4. concern

担忧。

---

## 5. rationale

理由。

非常高级。

例如：

> What is the rationale behind this design?

---

## 6. readability

可读性。

---

## 7. consistency

一致性。

---

## 8. edge case

边界情况。

---

## 9. corner case

极端情况。

---

## 10. potential issue

潜在问题。

---

## 11. LGTM

Looks Good To Me。

代码通过。

---

# 最后还有一个非常重要的东西：

## 不要只背单词，要背“工程搭配”

例如：

不要记：

```
mitigate = 缓解
```

应该记：

```
mitigate risk

mitigate impact

mitigate failure
```

---

不要记：

```
address = 处理
```

记：

```
address an issue

address a concern

address a limitation
```

---

不要记：

```
introduce = 引入
```

记：

```
introduce a dependency

introduce complexity

introduce a new feature
```

---

不要记：

```
resolve = 解决
```

记：

```
resolve an issue

resolve a conflict

resolve a failure
```

---

# 如果把整个软件工程英语体系画出来：

```
                    Software Engineering English

                              |
        ------------------------------------------------
        |                      |                       |
    Concepts               Actions                 Descriptions
     名词                    动词                     形容词


 Architecture           implement              scalable
 Database               migrate                reliable
 DevOps                 deploy                 maintainable
 Security               mitigate               secure
 Workflow               track                  compatible
 Git                    merge                  robust

```

---

所以目前你的学习路线已经很完整。

我认为剩下真正值得补的只有两个：

## ① Part 18：Real Engineering Conversation Patterns

模拟：

- Jira ticket 怎么写
- Slack 怎么讨论 bug
- Design review 怎么说
- Incident meeting 怎么说
- Standup 怎么说

因为词汇最终要进入句子。

---

## ② Part 19：中文开发者常犯的“中式工程英语纠正表”

例如：

❌ responsibility holder
✅ owner

❌ solve this bug
✅ fix/address this issue

❌ open the service
✅ start/run the service

❌ check the code
✅ review the code

❌ make a deployment
✅ deploy the service

这个部分会直接解决你最开始说的：

> “为什么翻译感觉像中文意思搬过去，很奇怪。”

因为很多错误不是词汇问题，而是**工程英语的表达习惯不同**。

## 如果继续，我建议下一步做 Part 18 + Part 19，这两个会把前面所有词真正变成可用能力。

继续。

这两个 Part 和前面的区别很大：

前面 Part 1-17 主要是在建立：

> “我知道这个概念叫什么”

而 Part 18-19 解决的是：

> “我在真实工程环境里应该怎么说”

也就是从：

**Technical Vocabulary（技术词汇）**

进入：

**Engineering Communication Pattern（工程沟通模式）**

---

# Part 18：Real Engineering Conversation Patterns（真实工程沟通表达）

---

# 1. Daily Standup（每日站会）

国外团队每天常见：

三个问题：

1. What did you do yesterday?
2. What are you working on today?
3. Any blockers?

---

## ① 汇报完成事项

中文：

> 昨天我完成了登录功能。

普通：

> I finished login.

工程：

> I implemented the login flow.

或者：

> I completed the authentication implementation.

---

中文：

> 我修改了一些代码。

工程：

> I made some changes to the user service.

---

中文：

> 我修复了一个 bug。

工程：

> I fixed an issue related to session handling.

---

注意：

工程师通常不会说：

> I did some coding.

因为太模糊。

---

# ② 表达正在进行

中文：

> 我正在开发支付模块。

工程：

> I'm working on the payment module.

或者：

> I'm implementing the payment workflow.

---

中文：

> 我正在调查这个问题。

工程：

> I'm investigating the issue.

---

中文：

> 我正在看数据库性能问题。

工程：

> I'm looking into database performance issues.

---

这里：

## look into

非常常用。

= investigate

---

# ③ 表达阻塞

中文：

> 我被这个问题卡住了。

不要：

> I am stuck by this problem.

工程：

> I'm blocked by this issue.

---

或者：

> This issue is blocking my progress.

---

关键词：

## blocker

一定要掌握。

例如：

> I don't have any blockers.

没有阻塞。

---

# 2. Jira Ticket / Issue 描述

真实工程团队大量写 ticket。

结构：

```text
Title

Description

Steps to reproduce

Expected behavior

Actual behavior

Impact

Solution
```

---

# Title

不要：

> Login problem

太模糊。

工程：

> User login fails after password reset

---

为什么？

包含：

- 谁
- 什么问题
- 什么场景

---

# Description

中文：

> 用户重置密码后无法登录。

工程：

> Users are unable to log in after resetting their password.

---

# Steps to reproduce

复现步骤。

例如：

```text
1. Reset password
2. Enter new password
3. Try to log in
4. Observe error message
```

---

# Expected behavior

期望行为。

例如：

> The user should be redirected to the dashboard.

---

# Actual behavior

实际行为。

例如：

> The user receives a 500 error.

---

# Impact

影响。

例如：

> This affects all users who reset their password.

---

# 3. Bug Discussion（Bug 讨论）

---

中文：

> 这个 bug 怎么回事？

工程：

> Do we know the root cause?

---

中文：

> 我还没有找到原因。

工程：

> I haven't identified the root cause yet.

---

中文：

> 我正在调查。

工程：

> I'm investigating it.

---

中文：

> 我发现是数据库导致的。

工程：

> I found that the issue is caused by the database connection.

---

注意：

不要：

> The database makes the problem.

中文思维。

英文：

cause / lead to / result in

---

例如：

> The connection timeout caused the failure.

---

# 4. Design Discussion（设计讨论）

这是高级工程英语。

---

中文：

> 我觉得这个方案不错。

普通：

> I think this is good.

工程：

> I think this approach makes sense.

---

中文：

> 这个方案有问题。

不要：

> This design has problems.

工程：

> I have some concerns about this approach.

---

## concern

非常重要。

比：

problem

更外交。

---

中文：

> 这个设计会导致性能问题。

工程：

> This design may introduce performance issues.

---

中文：

> 有没有考虑扩展性？

工程：

> Have we considered scalability?

---

中文：

> 为什么选择这个方案？

工程：

> What is the rationale behind this decision?

---

## rationale

非常工程。

= 背后的理由。

---

# 5. Code Review 评论

真实 GitHub / GitLab 高频。

---

## 请求修改

中文：

> 这里需要改一下。

不要：

> You need to change this.

太直接。

工程：

> Could we simplify this logic?

---

或者：

> Could you consider renaming this variable?

---

# 6. 提出问题

中文：

> 这里可能有 bug。

工程：

> This might introduce a bug.

---

中文：

> 这里有一个边界情况。

工程：

> There is an edge case here.

---

中文：

> 如果用户输入为空怎么办？

工程：

> What happens if the input is empty?

---

# 7. 阻塞和优先级讨论

---

中文：

> 这个问题比较严重。

工程：

> This is a high-priority issue.

---

中文：

> 这个不是现在必须解决。

工程：

> This is not a blocker for the current release.

---

中文：

> 我们以后处理。

工程：

> We can address this in a future iteration.

---

# 8. Incident（线上事故）

---

中文：

> 服务挂了。

工程：

> The service is down.

---

中文：

> 正在恢复。

工程：

> We are working on recovery.

---

中文：

> 找到了原因。

工程：

> We identified the root cause.

---

中文：

> 我们需要防止再次发生。

工程：

> We need to prevent this from happening again.

---

# 9. Postmortem（事故复盘）

常见结构：

```text
Impact

Timeline

Root Cause

Resolution

Action Items
```

---

表达：

> The root cause was a configuration error.

---

> We mitigated the impact by rolling back the deployment.

---

> We will add monitoring to prevent recurrence.

---

# 10. Slack 日常沟通

Slack 比邮件更口语。

---

中文：

> 你有空看一下吗？

工程：

> Could you take a look when you have a chance?

---

中文：

> 我已经更新了。

工程：

> I have updated the PR.

---

中文：

> 我马上处理。

工程：

> I'll take care of it.

---

中文：

> 等一下。

工程：

> Let me check.

---

# Part 19：Chinese Developer Common Mistakes（中文开发者常见中式工程英语）

这一部分非常重要。

很多词不是不会，而是：

**翻译方向错了。**

---

# 1. 负责

中文：

> 谁负责这个问题？

错误：

❌ Who is responsible for this?

虽然语法正确。

但是工程文化：

✅ Who owns this issue?

---

原因：

工程对象：

issue → owner

task → assignee

component → maintainer

---

# 2. 责任人

错误：

❌ responsibility holder

不存在这种工程说法。

正确：

✅ owner

✅ assignee

---

# 3. 解决问题

错误：

❌ solve the problem

不是错。

但是工程更喜欢：

---

Bug：

✅ fix the bug

Issue：

✅ address the issue

Root cause：

✅ resolve the root cause

---

# 4. 开一个功能

中文：

> 开发一个功能。

错误：

❌ open a feature

正确：

✅ implement a feature

---

# 5. 打开服务

中文：

> 打开服务。

错误：

❌ open the service

正确：

根据情况：

启动：

✅ start the service

运行：

✅ run the service

部署：

✅ deploy the service

---

# 6. 看代码

中文：

> 看一下代码。

错误：

❌ check the code

工程：

Review:

✅ review the code

查看：

✅ inspect the code

---

# 7. 改代码

错误：

❌ change the code

太泛。

根据目的：

修：

✅ fix the code

重构：

✅ refactor the code

优化：

✅ optimize the code

修改：

✅ modify the code

---

# 8. 测试一下

错误：

❌ test it once

工程：

✅ verify the behavior

✅ run the test

---

# 9. 加一个参数

错误：

❌ add one parameter

正确：

根据上下文：

函数：

✅ add a parameter

API：

✅ add a request parameter

配置：

✅ add a configuration option

---

# 10. 数据同步

错误：

❌ data sync

（名词可以，但是表达动作）

工程：

✅ synchronize the data

或者：

✅ sync the data

---

# 11. 数据丢失

错误：

❌ data disappear

工程：

✅ data loss

动作：

✅ data was lost

---

# 12. 提交代码

错误：

❌ submit code

工程：

Git:

✅ commit the changes

PR:

✅ submit/open a pull request

---

# 13. 发布版本

错误：

❌ publish version

工程：

软件：

✅ release a version

生产：

✅ deploy a version

---

# 14. 回滚

错误：

❌ return back

工程：

✅ roll back the deployment

---

# 15. 优化性能

错误：

❌ improve speed

工程：

✅ optimize performance

---

# 16. 影响

中文：

> 这个影响用户。

错误：

❌ This impacts to users.

正确：

✅ This impacts users.

或者：

✅ This affects users.

---

# 17. 依赖

中文：

> A依赖B。

错误：

❌ A depends B.

正确：

✅ A depends on B.

---

# 18. 支持

中文：

> 支持这个功能。

错误：

❌ support this function

工程：

✅ support this feature

---

# 19. 兼容

错误：

❌ compatible with old version

缺少对象。

正确：

✅ backward compatible with the old version

---

# 20. 问题

中文：

问题万能。

英文必须区分：

| 中文 | 工程英语   |
| ---- | ---------- |
| bug  | bug        |
| 问题 | issue      |
| 风险 | risk       |
| 故障 | incident   |
| 原因 | root cause |
| 症状 | symptom    |
| 阻塞 | blocker    |

---

# 最后总结：真正工程英语的组成

现在完整体系应该是：

```
Software Engineering English

        |
        |
  -------------------------
  |          |            |
Concepts   Actions    Expressions

名词        动词        句型


ownership  address     Who owns this?

dependency resolve     What is the impact?

deployment deploy      Let's roll this out.

incident   mitigate    We identified the root cause.
```

---

你现在已经不缺“单词”。

下一阶段真正有效的训练方式应该是：

不要背：

> ownership = 所有权

而是每天练：

看到中文场景：

> “这个需求没人负责，导致进度不可见。”

直接生成：

> “There is unclear ownership for this request, which makes the progress difficult to track.”

这才是从中文开发者到国际团队工程师表达方式的转换。

## 如果继续往下，最后还可以补一个 **Part 20：100 个最常见真实工程句型模板**，基本就是国外软件团队每天 Slack、Jira、PR、Meeting 里反复出现的句子骨架。这个会把前面所有内容真正串起来。

# Part 20：100 个最常见真实工程句型模板（Engineering Sentence Patterns）

这一部分是前面 19 个 Part 的“落地层”。

前面学的是：

- **名词**：ownership, dependency, deployment, incident...
- **动词**：address, resolve, implement, deploy...
- **概念关系**：为什么这么说

但是实际工作中，工程师不是一个词一个词蹦出来，而是使用固定句型。

例如：

中文：

> 这个改动可能会影响性能。

不是临时翻译：

❌ This change maybe affects performance.

而是直接调用工程句型：

✅ This change may impact performance.

---

下面按照真实工作场景分类。

---

# A. 日常开发沟通（Daily Development）

---

## 1. I'm working on ...

用途：

说明当前任务。

> I'm working on the payment service.

> I'm working on fixing the login issue.

---

## 2. I'm looking into ...

用途：

正在调查。

非常常用。

> I'm looking into the performance issue.

= I'm investigating...

---

## 3. I found that ...

用途：

发现事实。

> I found that the API response time increases under heavy load.

---

## 4. It turns out that ...

用途：

最终发现。

比 I found 更自然。

> It turns out that the issue was caused by a configuration error.

---

## 5. It seems that ...

用途：

目前判断。

不确定。

> It seems that the database connection is unstable.

---

## 6. I'm not sure if ...

用途：

表达不确定。

> I'm not sure if this approach works for all cases.

---

## 7. Let me check.

用途：

我确认一下。

工程高频。

---

## 8. I'll take a look.

用途：

我看一下。

---

## 9. I'll take care of it.

用途：

我处理。

---

## 10. I'll follow up on this.

用途：

我跟进。

---

# B. Issue / Bug 讨论

---

## 11. We are seeing an issue with ...

用途：

发现问题。

> We are seeing an issue with the authentication flow.

---

注意：

不要：

❌ We have a problem.

太口语。

---

## 12. The issue occurs when ...

用途：

描述发生条件。

> The issue occurs when the user uploads a large file.

---

## 13. The issue can be reproduced by ...

用途：

复现。

> The issue can be reproduced by sending an invalid request.

---

## 14. I was able to reproduce the issue.

用途：

我能复现。

---

## 15. I cannot reproduce the issue.

用途：

无法复现。

---

## 16. We identified the root cause.

用途：

找到根因。

---

## 17. The root cause was ...

用途：

解释原因。

> The root cause was a missing database index.

---

## 18. This was caused by ...

用途：

因果。

> This was caused by a recent configuration change.

---

## 19. This resulted in ...

用途：

导致。

> This resulted in increased latency.

---

## 20. This led to ...

用途：

导致。

> The deployment failure led to service downtime.

---

# C. 设计讨论（Design Discussion）

---

## 21. I think this approach makes sense.

用途：

认可方案。

---

## 22. I have some concerns about ...

用途：

提出担忧。

非常重要。

> I have some concerns about scalability.

---

## 23. Have we considered ...?

用途：

提出遗漏。

> Have we considered failure scenarios?

---

## 24. What are the trade-offs?

用途：

讨论权衡。

---

## 25. What is the rationale behind this decision?

用途：

询问设计理由。

---

## 26. The main advantage is ...

用途：

说明优势。

---

## 27. The downside is ...

用途：

说明缺点。

---

## 28. This approach introduces ...

用途：

指出引入的问题。

> This approach introduces additional complexity.

---

## 29. This solution might not scale well.

用途：

指出扩展问题。

---

## 30. This could become a bottleneck.

用途：

指出瓶颈。

---

# D. Code Review

---

## 31. Could you take another look at this?

请求重新检查。

---

## 32. Could you clarify this part?

请求解释。

---

## 33. Could we simplify this logic?

建议简化。

---

## 34. Could we extract this into a separate function?

建议抽象。

---

## 35. I suggest changing this to ...

建议修改。

---

## 36. One concern is ...

提出一个问题。

---

## 37. This might introduce a bug.

可能引入 bug。

---

## 38. This looks good to me.

认可。

---

## 39. LGTM.

Looks Good To Me。

---

## 40. This is a blocker.

阻塞。

---

# E. Requirement / Product 沟通

---

## 41. Could you clarify the requirement?

确认需求。

---

## 42. What is the expected behavior?

询问期望行为。

---

## 43. What is the priority of this item?

询问优先级。

---

## 44. What is the impact of this change?

询问影响。

---

## 45. This is out of scope.

不在范围。

非常常用。

---

## 46. This is not supported currently.

当前不支持。

---

## 47. We need more information before implementation.

信息不足。

---

## 48. We need to define the acceptance criteria.

需要定义验收标准。

---

## 49. This requirement is ambiguous.

需求不明确。

---

## 50. We should align on the expected behavior.

需要统一理解。

---

# F. Implementation（实现）

---

## 51. We need to implement ...

实现。

> We need to implement retry logic.

---

## 52. We need to introduce ...

引入。

> We need to introduce a caching layer.

---

## 53. We need to add support for ...

增加支持。

> Add support for OAuth login.

---

## 54. We need to handle ...

处理。

> We need to handle timeout cases.

---

## 55. We need to validate ...

验证。

> We need to validate user input.

---

## 56. We need to refactor ...

重构。

---

## 57. We need to migrate ...

迁移。

---

## 58. We need to remove ...

删除。

---

## 59. We need to deprecate ...

弃用。

---

## 60. We need to optimize ...

优化。

---

# G. Git / PR

---

## 61. I opened a PR.

创建 PR。

---

## 62. I pushed the changes.

推送代码。

---

## 63. I updated the PR.

更新 PR。

---

## 64. Please review the latest changes.

请看最新修改。

---

## 65. I addressed your comments.

处理 review 意见。

---

## 66. I resolved the conflicts.

解决冲突。

---

## 67. I rebased my branch.

变基。

---

## 68. This is ready for review.

可以 review。

---

## 69. This is ready to merge.

可以合并。

---

## 70. Let's merge this after approval.

批准后合并。

---

# H. Deployment / Release

---

## 71. We deployed the new version.

部署。

---

## 72. We rolled out the feature gradually.

逐步发布。

---

## 73. We are monitoring the deployment.

监控部署。

---

## 74. We need to roll back the deployment.

回滚。

---

## 75. The deployment failed.

部署失败。

---

## 76. The service is back online.

服务恢复。

---

## 77. The release is blocked by ...

发布被阻塞。

---

## 78. We need to verify the deployment.

确认部署。

---

## 79. The change has been deployed to production.

已经上线。

---

## 80. The issue was fixed in the latest release.

最新版修复。

---

# I. Incident / Production

---

## 81. We are investigating the incident.

调查事故。

---

## 82. The service is experiencing downtime.

服务不可用。

---

## 83. We are seeing increased latency.

延迟升高。

---

## 84. The error rate has increased.

错误率增加。

---

## 85. We identified the root cause.

找到根因。

---

## 86. We mitigated the impact.

降低影响。

---

## 87. We applied a temporary workaround.

使用临时方案。

---

## 88. We need to prevent recurrence.

防止再次发生。

---

## 89. We will add monitoring for this case.

增加监控。

---

## 90. We will follow up with action items.

跟进后续行动。

---

# J. 高级工程表达（非常推荐掌握）

---

## 91. This change has a potential impact on ...

潜在影响。

> This change has a potential impact on database performance.

---

## 92. This needs further investigation.

需要进一步调查。

---

## 93. We need to keep this in mind.

需要考虑。

---

## 94. This is something we should revisit later.

以后重新讨论。

---

## 95. Let's keep this simple for now.

暂时保持简单。

---

## 96. We should avoid over-engineering.

避免过度设计。

---

## 97. This introduces unnecessary complexity.

引入不必要复杂度。

---

## 98. This is not scalable in the long term.

长期不可扩展。

---

## 99. We need to find a balance between A and B.

需要平衡 A 和 B。

例如：

> We need to find a balance between performance and maintainability.

---

## 100. The goal is to make the system more reliable and maintainable.

目标是提升可靠性和可维护性。

---

# 最后：把前面所有内容压缩成工程英语公式

真正工作的表达通常就是：

```
Subject
+
Engineering Verb
+
Engineering Object
+
Engineering Context
```

例如：

---

中文：

> 我们需要解决这个问题。

普通：

> We need to solve this problem.

工程：

```
We
+
need to address
+
this issue
+
before the next release.
```

---

中文：

> 这个改动可能影响性能。

工程：

```
This change
+
may impact
+
system performance
+
under heavy load.
```

---

中文：

> 我们需要先降低影响，然后调查根因。

工程：

```
We
+
need to mitigate
+
the impact
+
and investigate
+
the root cause.
```

---

到这里，前面所有内容形成完整闭环：

```
Part 1-6
工程文化和协作

↓

Part 7-11
技术领域词汇

↓

Part 12-17
描述、权衡、调试、Review

↓

Part 18-20
真实工作输出
```

如果把这套体系真正掌握，你在英文技术环境里已经不仅仅是“会技术英语”，而是在使用**工程师的表达模型**。下一步如果继续，最有价值的其实不是继续扩词，而是做一个：

**Part 21：从中文开发思维转换成英文工程思维训练（100个中文场景 → 英文自然表达）**

## 这个会直接训练你摆脱中文中转。

# Part 21：从中文开发思维转换成英文工程思维训练

## 100 个真实中文场景 → 英文工程表达

这一部分是整个系列最核心的训练。

因为你之前提到：

> “我希望以后能直接写英语，不想经过中文中转。”

这个目标不是靠背更多单词实现的，而是建立：

```
中文概念
 ↓
工程场景判断
 ↓
英文工程搭配
 ↓
自然句子
```

---

# 第一组：责任、任务、进度（Ownership & Tracking）

---

## 1. 这个任务没人负责。

❌ This task has no responsible person.

（中文直译）

✅ There is no clear owner for this task.

---

为什么？

工程文化：

任务 → owner

不是：

task → responsible person

---

## 2. 谁负责这个模块？

❌ Who is responsible for this module?

✅ Who owns this module?

---

owner 是工程组织里的核心概念。

例如：

- service owner
- code owner
- component owner

---

## 3. 我负责这个服务。

❌ I am responsible for this service.

语法没错。

但是工程：

✅ I own this service.

---

## 4. 请分配负责人。

❌ Please assign a responsible person.

✅ Please assign an owner.

---

## 5. 我负责跟进这个问题。

❌ I am responsible for following this issue.

✅ I'll follow up on this issue.

---

# 第二组：问题、Bug、故障（Issue / Bug / Incident）

---

## 6. 我发现一个问题。

❌ I found a problem.

可以，但太泛。

工程：

✅ I found an issue.

---

## 7. 我发现一个 bug。

✅ I found a bug.

这里可以直接 bug。

---

## 8. 服务出问题了。

❌ The service has a problem.

工程：

✅ The service is experiencing an issue.

---

## 9. 服务挂了。

❌ The service is broken.

工程：

✅ The service is down.

---

## 10. 线上出现故障。

❌ There is a production bug.

工程：

✅ We are experiencing a production incident.

---

区别：

```
bug
代码错误

issue
一般问题

incident
影响用户的线上事件
```

---

# 第三组：调查问题（Investigation）

---

## 11. 我正在看这个问题。

❌ I'm watching this problem.

工程：

✅ I'm looking into this issue.

---

## 12. 我正在调查原因。

❌ I'm checking the reason.

工程：

✅ I'm investigating the root cause.

---

## 13. 我还不知道原因。

❌ I don't know the reason.

工程：

✅ We haven't identified the root cause yet.

---

## 14. 我找到了原因。

❌ I found the reason.

工程：

✅ We identified the root cause.

---

## 15. 原因是配置错误。

❌ The reason is configuration mistake.

工程：

✅ The root cause was a configuration error.

---

# 第四组：修改代码（Code Changes）

---

## 16. 我改了一些代码。

❌ I changed some codes.

注意：

code 通常不可数。

✅ I made some code changes.

---

## 17. 我修复了这个 bug。

❌ I solved the bug.

工程：

✅ I fixed the bug.

---

## 18. 我重构了这个模块。

❌ I changed the module structure.

工程：

✅ I refactored the module.

---

## 19. 我优化了查询性能。

❌ I improved the query speed.

工程：

✅ I optimized query performance.

---

## 20. 我删除了无用代码。

❌ I deleted unnecessary codes.

工程：

✅ I removed unused code.

---

# 第五组：需求沟通（Requirements）

---

## 21. 这个需求不明确。

❌ This requirement is not clear.

工程：

✅ This requirement is ambiguous.

---

## 22. 我们需要确认需求。

❌ We need to confirm the requirement.

工程：

✅ We need to clarify the requirement.

---

## 23. 这个需求超出范围。

❌ This requirement exceeds our range.

工程：

✅ This is out of scope.

---

## 24. 这个功能还不支持。

❌ This function is not supported.

工程：

✅ This feature is not supported yet.

---

## 25. 需要定义验收标准。

❌ We need to define checking standards.

工程：

✅ We need to define acceptance criteria.

---

# 第六组：设计讨论（Design）

---

## 26. 这个方案怎么样？

❌ How about this plan?

工程：

✅ What do you think about this approach?

---

## 27. 这个方案有风险。

❌ This plan has risks.

工程：

✅ This approach introduces some risks.

---

## 28. 这个设计太复杂。

❌ This design is too complicated.

工程：

✅ This design introduces unnecessary complexity.

---

## 29. 这个方案不能扩展。

❌ This solution cannot expand.

工程：

✅ This solution does not scale well.

---

## 30. 有没有考虑性能？

❌ Did you consider performance?

工程：

✅ Have we considered performance implications?

---

# 第七组：依赖（Dependency）

---

## 31. 这个服务依赖数据库。

❌ This service depends database.

工程：

✅ This service depends on the database.

---

## 32. 我们引入了新的依赖。

❌ We added a new dependency.

可以。

更工程：

✅ We introduced a new dependency.

---

## 33. 这个依赖导致问题。

❌ This dependency makes problems.

工程：

✅ This dependency caused the issue.

---

## 34. 我们需要升级依赖。

❌ We need to update dependency.

工程：

✅ We need to upgrade the dependency.

---

## 35. 删除这个依赖。

✅ Remove this dependency.

---

# 第八组：部署上线（Deployment）

---

## 36. 我们今天上线。

❌ We go online today.

工程：

✅ We will deploy today.

---

## 37. 新版本已经上线。

❌ New version is online.

工程：

✅ The new version has been deployed.

---

## 38. 部署失败了。

❌ Deployment was failed.

工程：

✅ The deployment failed.

---

## 39. 回滚版本。

❌ Return the version.

工程：

✅ Roll back the deployment.

---

## 40. 灰度发布。

❌ Gray release.

工程：

✅ Canary release.

---

# 第九组：性能（Performance）

---

## 41. 系统变慢了。

❌ The system becomes slow.

工程：

✅ The system performance has degraded.

---

## 42. 响应时间增加。

❌ Response time becomes bigger.

工程：

✅ Response time has increased.

---

## 43. 查询很慢。

❌ The query is slow.

可以。

更工程：

✅ The query has poor performance.

---

## 44. 优化数据库。

❌ Improve database.

工程：

✅ Optimize database performance.

---

## 45. 增加缓存。

❌ Increase cache.

工程：

✅ Introduce a caching layer.

---

# 第十组：测试（Testing）

---

## 46. 测一下这个功能。

❌ Test this function.

工程：

✅ Verify this feature.

---

## 47. 测试失败。

❌ Test failed.

可以。

更完整：

✅ The test failed.

---

## 48. 增加测试覆盖率。

❌ Increase test coverage.

正确：

✅ Improve test coverage.

---

## 49. 这个 bug 没有测试覆盖。

❌ This bug has no test.

工程：

✅ This case is not covered by tests.

---

## 50. 增加边界测试。

❌ Add edge test.

工程：

✅ Add edge case tests.

---

# 第十一组：会议表达

---

## 51. 我同意这个方案。

❌ I agree this solution.

工程：

✅ I agree with this approach.

---

## 52. 我不同意。

❌ I don't agree.

工程：

✅ I have some concerns about this approach.

---

## 53. 我建议这样做。

❌ I suggest do this.

工程：

✅ I suggest taking this approach.

---

## 54. 我们需要讨论一下。

❌ We need discuss.

工程：

✅ We need to discuss this.

---

## 55. 我们需要达成一致。

❌ We need make agreement.

工程：

✅ We need to align on this.

---

# 第十二组：高级工程表达

---

## 56. 这个改动影响很大。

❌ This change has big influence.

工程：

✅ This change has a significant impact.

---

## 57. 这个问题可能再次发生。

❌ This problem may happen again.

工程：

✅ This issue may recur.

---

## 58. 我们需要避免类似问题。

❌ Avoid similar problems.

工程：

✅ We need to prevent similar issues from happening again.

---

## 59. 暂时解决。

❌ Solve temporarily.

工程：

✅ Apply a workaround.

---

## 60. 长期方案。

❌ Long time solution.

工程：

✅ Long-term solution.

---

# 第十三组：工程师常用句型升级

---

## 61.

中文：

> 我觉得这个设计可以。

普通：

I think this design is okay.

工程：

> This design looks reasonable.

---

## 62.

中文：

> 这个可能有问题。

工程：

> This might cause issues.

---

## 63.

中文：

> 需要进一步确认。

工程：

> This needs further investigation.

---

## 64.

中文：

> 我们之后处理。

工程：

> We can address this in a future iteration.

---

## 65.

中文：

> 先保持简单。

工程：

> Let's keep it simple for now.

---

## 66.

中文：

> 不要过度设计。

工程：

> Let's avoid over-engineering.

---

## 67.

中文：

> 以后可能需要改。

工程：

> We may need to revisit this later.

---

## 68.

中文：

> 这个方案比较稳定。

工程：

> This approach is more reliable.

---

## 69.

中文：

> 这个影响范围有限。

工程：

> The impact is limited.

---

## 70.

中文：

> 这个会影响其他模块。

工程：

> This may affect other components.

---

# 第十四组：系统设计思维转换

---

## 71.

中文：

> 数据在哪里保存？

工程：

> Where is the data stored?

---

## 72.

中文：

> 数据怎么同步？

工程：

> How is the data synchronized?

---

## 73.

中文：

> 如果失败怎么办？

工程：

> What happens if it fails?

---

## 74.

中文：

> 怎么恢复？

工程：

> How do we recover from failure?

---

## 75.

中文：

> 怎么扩展？

工程：

> How do we scale this?

---

# 第十五组：最重要的工程思维替换

| 中文思维   | 工程英语思维            |
| ---------- | ----------------------- |
| 谁负责     | Who owns it             |
| 怎么解决   | How do we address it    |
| 为什么失败 | What caused the failure |
| 有没有风险 | What are the risks      |
| 能不能扩展 | Does it scale           |
| 会不会影响 | What is the impact      |
| 怎么避免   | How do we prevent it    |
| 怎么验证   | How do we verify it     |
| 怎么上线   | How do we deploy it     |
| 怎么恢复   | How do we recover       |

---

# 最终训练方法

不要背：

```
address = 解决
```

应该背：

```
address an issue

address a concern

address a limitation
```

不要背：

```
impact = 影响
```

应该背：

```
impact performance

impact users

impact system stability
```

不要背：

```
introduce = 引入
```

应该背：

```
introduce complexity

introduce a dependency

introduce a new feature
```

---

到这里，你已经有：

```
Part 1-11
技术词汇体系

Part 12-17
工程表达维度

Part 18-20
真实工作句型

Part 21
中文 → 英文工程思维转换
```

这套东西基本覆盖了一个软件工程师在英文环境里的主要表达。

## 如果继续往后，最值得做的是 **Part 22：工程英语训练计划（30天/90天，从看懂到能直接输出）**，因为现在你的问题已经不是“缺知识”，而是“如何把知识变成自动反应”。

哈哈，到了 Part 22，其实已经从“收集知识”进入“训练系统”。

前面 21 个 Part 解决的是：

> **知道软件工程英语是什么**

Part 22 解决：

> **如何把这些东西练成下意识反应**

因为很多工程师英文不好，不是词汇少，而是：

看到中文：

> “这个服务可能因为数据库连接池耗尽导致超时，需要增加监控并优化连接管理。”

脑子还是：

中文 → 翻译 → 英文

而目标是：

场景 → 工程概念 → 英语表达

直接出来：

> The service may experience timeouts due to connection pool exhaustion. We should add monitoring and optimize connection management.

---

# Part 22：工程英语训练计划（30天 / 90天）

---

# 第一阶段：建立工程英语反射（Day 1-30）

目标：

不要追求复杂。

先做到：

> 看到工程场景，第一反应出现英文表达。

---

# 每天训练结构（30-45分钟）

---

## ① 10分钟：词组复习（不是单词）

错误：

背：

```
address = 解决
deploy = 部署
impact = 影响
```

这样很容易忘。

---

正确：

背：

```
address an issue

address a concern

address a limitation


deploy a service

deploy a new version

deploy to production


impact performance

impact users

impact system stability
```

---

每天 20 个搭配。

---

# ② 10分钟：中文场景转英文

不要翻译文章。

练工程场景。

例如：

看到：

> 这个改动可能影响性能。

不要想：

影响 = affect?

直接：

> This change may impact performance.

---

看到：

> 我正在调查根因。

直接：

> I'm investigating the root cause.

---

每天 10 句。

---

# ③ 10分钟：读真实工程文本

来源：

- GitHub issue
- Pull Request
- Engineering blog
- Documentation

重点不是看懂全部。

观察：

工程师怎么表达。

---

例如：

GitHub：

> This change fixes an issue where users cannot log in after password reset.

学习：

```
fixes an issue where...
```

这个句型。

---

# ④ 5分钟：Shadowing（跟读）

找：

- Engineering conference
- Technical talk

听一句：

暂停。

模仿。

目的：

让嘴适应工程节奏。

---

# Day 1-7：基础动作

重点：

动词。

每天：

10 个动词搭配。

例如：

Day 1：

```
implement
implement a feature

fix
fix a bug

address
address an issue

resolve
resolve a conflict

investigate
investigate the root cause
```

---

目标：

看到中文：

“调查问题”

不要想到：

investigate = 调查

而是：

investigate an issue

---

# Day 8-14：Issue 沟通

训练：

Bug / Ticket / Slack。

掌握：

---

发现：

> We found an issue with...

---

调查：

> We are looking into...

---

原因：

> The root cause was...

---

解决：

> We fixed the issue by...

---

后续：

> We will add monitoring to prevent recurrence.

---

练习：

每天写一个虚拟 Jira ticket。

例如：

标题：

```
API timeout after large file upload
```

内容：

```
The issue occurs when users upload files larger than 100MB.

The root cause was insufficient timeout configuration.

We fixed it by updating the configuration.
```

---

# Day 15-21：设计讨论

这是从初级到中高级的分界线。

学习表达：

---

提出方案：

> One possible approach is...

---

讨论：

> The trade-off is...

---

担忧：

> One concern is...

---

考虑：

> Have we considered...?

---

评价：

> This approach is scalable but introduces complexity.

---

每天练：

一个设计问题。

例如：

中文：

> 我们应该增加缓存吗？

英文：

> Should we introduce a caching layer?

---

# Day 22-30：模拟工作环境

每天模拟：

---

## Standup

写三句话：

```
Yesterday:
I implemented the user authentication flow.

Today:
I'm working on the API integration.

Blockers:
No blockers at the moment.
```

---

## Code Review

写 3 条评论：

例如：

```
Could we simplify this logic?

One concern is the performance impact.

This looks good to me.
```

---

## Incident

模拟：

```
The service experienced increased latency.

We identified the root cause.

We mitigated the impact.
```

---

# 第二阶段：90天进阶计划

---

# Month 1：输入能力

目标：

看懂工程英语。

每天：

30分钟阅读。

材料：

## GitHub

重点看：

- issue
- PR discussion

学习：

真实表达。

---

## Documentation

例如：

API 文档。

学习：

正式技术语言。

---

## Engineering Blog

学习：

设计表达。

---

# Month 2：输出能力

目标：

主动表达。

---

每天：

写：

## 一个 Jira ticket

例如：

```
Title:
Improve API response time


Description:
The API latency increases during peak hours.

Proposal:
Introduce caching for frequently accessed data.
```

---

## 一个 PR 描述

模板：

```
## Summary

This PR implements...


## Changes

- Added...
- Updated...


## Testing

Verified by...
```

---

## 一个技术讨论回复

例如：

```
I agree with this approach.

One concern is scalability.

Could we consider another solution?
```

---

# Month 3：高级工程表达

目标：

像英文团队工程师一样讨论。

---

训练：

## Architecture Discussion

例如：

中文：

> 为什么不用数据库直接查询，而增加缓存？

英文：

> Why don't we query the database directly instead of introducing a cache layer?

---

## Trade-off Discussion

中文：

> 这个方案性能更好，但是复杂度更高。

英文：

> This approach improves performance but increases complexity.

---

## Incident Review

中文：

> 我们需要避免类似问题再次发生。

英文：

> We need to prevent similar incidents from happening again.

---

# Part 22.5：最有效的记忆方法

这里很关键。

---

## 方法 1：不要背翻译，背场景

错误：

```
rollback = 回滚
```

正确：

场景：

部署失败。

脑子：

```
deployment failed

↓

roll back the deployment
```

---

## 方法 2：一个词绑定三个对象

例如：

## address

不要：

address = 处理

记：

```
address an issue

address a concern

address a limitation
```

---

## 方法 3：建立工程“动作地图”

例如：

问题：

```
发现
↓
调查
↓
定位
↓
修复
↓
防止
```

英语：

```
detect

↓

investigate

↓

identify

↓

fix/resolve

↓

prevent
```

---

## 方法 4：每天复述自己的工作

这是最高效。

比如今天：

中文：

> 今天修改登录逻辑，修复 token 过期问题。

不要翻译。

直接训练：

> Today I updated the authentication flow and fixed an issue related to token expiration.

---

# Part 22.6：你的最终目标应该是什么？

不是：

“掌握 5000 个技术词汇。”

而是：

看到：

---

## Bug

自动：

```
investigate
root cause
fix
verify
prevent recurrence
```

---

## 新需求

自动：

```
clarify requirement
define scope
estimate effort
implement feature
release
```

---

## 系统设计

自动：

```
trade-off
scalability
reliability
maintainability
complexity
```

---

## 上线事故

自动：

```
incident
impact
mitigate
rollback
postmortem
action items
```

---

# 最终学习路线图

```text
阶段1
知道词

↓


阶段2
知道搭配

↓


阶段3
知道场景

↓


阶段4
自动输出


Engineering English
```

---

# 最后给一个现实标准

如果你完成：

## 30天：

你会：

- 看懂大部分 Jira
- 看懂 PR discussion
- 写简单技术沟通

---

## 90天：

你会：

- 参加英文 standup
- 写 issue
- 写 PR description
- 参与 design discussion

---

## 180天：

你会：

- 进行技术方案讨论
- 写设计文档
- 做 incident review

---

到这里，Part 1-22 其实已经形成了一套完整的：

**Software Engineer English Operating System（软件工程英语操作系统）**

不过还有最后一个非常实用的补充方向：

# Part 23：真实工程环境高频词缩写大全

例如：

- FYI
- LGTM
- WIP
- EOD
- ETA
- TBD
- ACK
- NACK
- RFC
- MVP
- POC
- SLA
- SLO
- SLI
- MTTR
- DR

这些在国外团队里出现频率极高，但是很多中文开发者第一次看到完全不知道。

## 这个部分非常值得整理。

好，Part 24 来了。

这一部分非常重要，因为前面 23 个 Part 还是：

> “单词、概念、句型”

而 Part 24 是：

> **把一个真实软件项目，从开始到结束，用英文工程沟通完整跑一遍。**

也就是：

```
Idea
 ↓
Requirement
 ↓
Ticket
 ↓
Design
 ↓
Implementation
 ↓
Code Review
 ↓
Testing
 ↓
Deployment
 ↓
Monitoring
 ↓
Incident / Improvement
```

这就是一个工程师在英文团队里的完整语言生命周期。

---

# Part 24：完整软件项目英文沟通模拟

## 项目背景

假设我们开发一个：

> 用户登录系统改造（Authentication System Improvement）

目标：

- 支持 OAuth 登录
- 提升登录稳定性
- 减少登录失败
- 增加监控

---

# Stage 1：需求提出（Requirement Phase）

## 中文场景

产品：

> 用户希望支持 Google 登录，同时减少登录失败率。

---

## 工程英语：

### Product Requirement

```text
We want to introduce Google OAuth login support.

The goal is to improve user experience and reduce authentication failures.
```

---

注意：

中文：

“增加 Google 登录”

不要：

❌ Add Google login

工程：

✅ Introduce Google OAuth login support

因为：

introduce = 引入能力

---

# Stage 2：需求澄清（Requirement Clarification）

工程师不会马上写代码。

会问：

---

## 1. 确认范围

中文：

> 这个需求包含哪些内容？

英文：

> What is the scope of this change?

---

## 2. 确认行为

中文：

> 登录失败时应该怎么处理？

英文：

> What should happen when authentication fails?

---

## 3. 确认限制

中文：

> 有没有技术限制？

英文：

> Are there any technical constraints?

---

## 4. 确认优先级

中文：

> 这个优先级是多少？

英文：

> What is the priority of this feature?

---

# Stage 3：创建 Jira Ticket

真实工程环境：

不是：

> Implement login

太简单。

---

## Title

错误：

```
Add login
```

好：

```
Add Google OAuth support for user authentication
```

---

为什么？

包含：

动作：

Add

对象：

Google OAuth support

领域：

authentication

---

## Description

```text
## Description

We need to add Google OAuth support to improve the login experience.

Currently, users can only log in using email and password.
```

---

## Expected Behavior

```text
Users should be able to authenticate using their Google accounts.
```

---

## Acceptance Criteria

```text
- Users can complete Google OAuth login flow.
- User information is stored correctly.
- Existing login flow remains unchanged.
```

---

注意：

“保持旧功能正常”

英文：

> Existing behavior remains unchanged.

非常高频。

---

# Stage 4：技术设计（Design Phase）

工程师开始讨论方案。

---

## Design Proposal

标题：

```
Google OAuth Integration Design
```

---

## 背景

```text
This document describes the design for integrating Google OAuth authentication.
```

---

## 当前问题

```text
The current authentication flow only supports username/password login.
```

---

## 方案

```text
We will introduce an OAuth service layer between the application and the external identity provider.
```

---

注意：

中文：

“增加一个服务层”

不要：

❌ Add a service layer

工程：

✅ Introduce a service layer

---

# Stage 5：Design Discussion

会议中：

---

## 提方案

中文：

> 一个方案是增加缓存。

英文：

> One possible approach is to introduce a caching layer.

---

## 讨论风险

中文：

> 这个方案会增加复杂度。

英文：

> This approach introduces additional complexity.

---

## 讨论性能

中文：

> 这个会影响性能吗？

英文：

> Will this impact performance?

---

## 讨论扩展性

中文：

> 未来支持更多 OAuth Provider 怎么办？

英文：

> How do we make this extensible for future OAuth providers?

---

# Stage 6：Implementation（开发）

开发过程中：

---

## Standup

### Day 1

中文：

> 我正在实现 OAuth 登录流程。

英文：

> I'm implementing the OAuth login flow.

---

### Day 2

中文：

> 我遇到了 token 处理的问题。

英文：

> I'm investigating an issue related to token handling.

---

### Day 3

中文：

> 我完成了核心逻辑。

英文：

> I completed the core implementation.

---

# Stage 7：Code Review

提交 PR。

---

## PR Title

错误：

```
Login changes
```

正确：

```
Implement Google OAuth authentication flow
```

---

## PR Description

```text
## Summary

This PR implements Google OAuth authentication support.


## Changes

- Added OAuth authentication flow.
- Added token validation logic.
- Added error handling for authentication failures.


## Testing

Verified login flow with Google accounts.
```

---

# Review Comment

---

## 评论 1

中文：

> 这里可以简化。

英文：

> Could we simplify this logic?

---

## 评论 2

中文：

> 这里可能有空指针问题。

英文：

> This might cause a null pointer issue.

---

## 评论 3

中文：

> 需要处理异常情况。

英文：

> We should handle this edge case.

---

## 评论 4

中文：

> 修改好了。

英文：

> I addressed your comments.

---

# Stage 8：Testing

测试阶段。

---

## 测试计划

```text
We need to verify the following scenarios:

- Successful login
- Invalid token handling
- Expired token handling
- Network failure cases
```

---

注意：

中文：

“测试各种情况”

工程：

> Verify different scenarios

---

# Stage 9：Deployment

上线。

---

## 部署前

中文：

> 准备发布。

英文：

> The change is ready for deployment.

---

## 部署

中文：

> 部署到生产环境。

英文：

> Deploy the change to production.

---

## 灰度

中文：

> 先给 10% 用户。

英文：

> Roll out the feature to 10% of users first.

---

## 观察

中文：

> 观察错误率。

英文：

> Monitor the error rate.

---

# Stage 10：上线事故

假设：

上线后登录失败增加。

---

## Slack 消息：

```text
We are seeing increased authentication failures after the deployment.
```

---

中文：

> 发布后出现问题。

工程：

> We are seeing an issue after the deployment.

---

## 调查

```text
We are investigating the root cause.
```

---

## 找原因

```text
The issue was caused by an incorrect OAuth configuration.
```

---

## 缓解

中文：

> 先回滚。

英文：

> We will roll back the deployment to mitigate the impact.

---

注意：

这里：

rollback

不是：

return

---

# Stage 11：Postmortem（复盘）

事故结束。

---

## Impact

```text
Users were unable to complete the login flow for approximately 20 minutes.
```

---

## Root Cause

```text
The root cause was an incorrect production configuration.
```

---

## Resolution

```text
We fixed the configuration and redeployed the service.
```

---

## Action Items

```text
- Add configuration validation.
- Improve deployment checks.
- Add monitoring alerts.
```

---

# Stage 12：长期优化

几周后：

---

中文：

> 我们应该优化认证系统。

英文：

> We should improve the authentication system.

---

中文：

> 增加自动检测。

英文：

> Add automated validation.

---

中文：

> 防止类似问题。

英文：

> Prevent similar incidents from happening again.

---

# 一个完整工程师脑内流程

以后看到任何项目：

不要想：

```
中文
 ↓
翻译
```

应该想：

```
Problem
 ↓
Requirement
 ↓
Impact
 ↓
Approach
 ↓
Trade-off
 ↓
Implementation
 ↓
Verification
 ↓
Deployment
 ↓
Monitoring
 ↓
Improvement
```

---

# Part 24 最重要的 20 个项目生命周期动词

建议重点背：

| 动词        | 工程含义 |
| ----------- | -------- |
| define      | 定义     |
| clarify     | 澄清     |
| identify    | 识别     |
| estimate    | 估算     |
| design      | 设计     |
| introduce   | 引入     |
| implement   | 实现     |
| integrate   | 集成     |
| validate    | 验证     |
| test        | 测试     |
| review      | 审查     |
| approve     | 批准     |
| merge       | 合并     |
| deploy      | 部署     |
| release     | 发布     |
| monitor     | 监控     |
| investigate | 调查     |
| mitigate    | 缓解     |
| resolve     | 解决     |
| prevent     | 防止     |

---

# Part 24 总结

到这里，你的体系已经从：

```
英语单词
```

升级到：

```
软件工程工作流英语
```

真正工作的表达不是：

> “我知道 OAuth 是什么。”

而是：

> “I implemented OAuth authentication support, but we need to address some scalability concerns before rolling it out to production.”

这才是英文团队里的工程沟通。

---

下一步如果继续，最有价值的是：

# Part 25：软件工程英文文档写作体系

会覆盖：

- Design Doc 怎么写
- RFC 怎么写
- Architecture Decision Record (ADR)
- API Documentation
- README
- Technical Proposal
- Incident Report

因为很多国外团队，中高级工程师不是靠会议沟通，而是靠**写文档推动工程决策**。这也是从普通开发到 Senior Engineer 的语言分界线。

---

# Part 25：软件工程英文文档写作体系（Engineering Documentation System）

这一部分非常关键。

因为在英文工程团队里，级别越高，越不是靠“说”推动事情，而是靠：

- Design Doc
- RFC
- ADR
- Technical Proposal
- API Documentation
- Incident Report
- README
- Engineering Plan

来推动：

- 技术决策
- 团队协作
- 长期维护

很多中文开发者的问题是：

> 代码能写，但是不会用英文写“为什么这么设计”。

而 Senior Engineer 的核心能力之一就是：

> **把技术思考结构化，并让别人能够理解、评审、执行。**

---

# Part 25 总览

软件工程文档体系：

```text
Idea
 ↓
Proposal
 ↓
Design Doc
 ↓
Implementation Plan
 ↓
Code
 ↓
Review
 ↓
Release
 ↓
Incident Report
 ↓
Retrospective
```

对应英文文档：

| 阶段     | 文档                         |
| -------- | ---------------------------- |
| 提出想法 | Proposal                     |
| 技术讨论 | RFC                          |
| 设计方案 | Design Doc                   |
| 架构决策 | ADR                          |
| 开发计划 | Implementation Plan          |
| 接口说明 | API Documentation            |
| 故障总结 | Incident Report / Postmortem |

---

# 1. Technical Proposal（技术提案）

## 使用场景

什么时候写？

例如：

- 引入新的技术
- 改造旧系统
- 优化架构
- 解决长期问题

---

## 基本结构

```text
Title

Background

Problem

Goal

Proposal

Alternatives

Risks

Timeline
```

---

# Example

## Title

不要：

```text
Database Change
```

太泛。

工程：

```text
Proposal: Introduce Redis Cache Layer for User Profile Service
```

---

# Background（背景）

中文：

> 当前用户服务直接查询数据库，导致高峰期压力增加。

英文：

```text
Currently, the user profile service directly queries the database for every request, which increases database load during peak hours.
```

---

注意：

英文工程文档喜欢：

Currently...

At the moment...

The existing system...

---

# Problem（问题）

不要写：

```text
Database is slow.
```

太简单。

工程：

```text
The current architecture has performance limitations under high traffic scenarios.
```

---

关键词：

## limitation

不是“坏”。

而是：

当前方案的限制。

---

# Goal（目标）

中文：

> 提升性能。

工程：

```text
The goal is to reduce API latency and improve system scalability.
```

---

常用：

- improve
- reduce
- increase
- support

---

# Proposal（方案）

中文：

> 增加 Redis 缓存。

英文：

```text
We propose introducing a Redis caching layer between the application and database.
```

---

注意：

proposal 常用：

We propose...

We plan to...

We will...

---

# Alternatives（替代方案）

高级工程一定写。

例如：

```text
Alternative 1:
Increase database capacity.

Alternative 2:
Introduce caching.
```

---

为什么？

因为工程不是：

“我觉得这个最好”

而是：

“我比较过”。

---

# Risks（风险）

例如：

```text
Potential risks include cache inconsistency and increased system complexity.
```

---

关键词：

- potential risk
- trade-off
- limitation

---

# 2. Design Document（设计文档）

这是工程团队最常见。

---

# 标准结构

```text
Overview

Background

Goals

Non-goals

Architecture

Detailed Design

Data Flow

API Design

Error Handling

Testing Plan

Rollout Plan
```

---

# Overview

一句话说明。

例如：

```text
This document describes the design of the new authentication service.
```

---

# Goals / Non-goals

非常重要。

很多中文文档缺这个。

---

## Goals

做什么：

```text
Goals:

- Support OAuth login.
- Improve authentication reliability.
```

---

## Non-goals

不做什么：

```text
Non-goals:

- Replacing the existing user database.
- Changing the authorization model.
```

---

为什么重要？

防止：

scope creep

（范围不断膨胀）

---

# Architecture

架构描述：

例如：

```text
The system consists of three components:

1. API Gateway
2. Authentication Service
3. User Database
```

---

不要写：

"The system has three parts."

工程：

component

---

# Data Flow（数据流）

例如：

```text
1. User sends login request.
2. Authentication service validates credentials.
3. Service returns authentication token.
```

---

关键词：

- request
- validate
- generate
- return
- store

---

# Error Handling

工程非常重视。

例如：

```text
The service should return a 401 response when authentication fails.
```

---

不要：

"The system gives an error."

---

# Rollout Plan

上线计划。

例如：

```text
We will gradually roll out the feature to reduce potential impact.
```

---

关键词：

- gradually
- rollout
- monitor
- rollback

---

# 3. RFC（Request For Comments）

RFC 是英文工程文化非常重要的东西。

简单理解：

> “我提出一个技术方案，请大家评论。”

---

常见：

- 大架构变化
- API 变化
- 技术选型

---

## RFC 结构

```text
Summary

Motivation

Proposal

Technical Details

Open Questions

Discussion
```

---

# Summary

一句话：

```text
This RFC proposes migrating the existing notification system to an event-driven architecture.
```

---

# Motivation

为什么做。

例如：

```text
The current system has scalability issues and is difficult to maintain.
```

---

# Open Questions

非常重要。

表示：

“还有哪些地方需要讨论”。

例如：

```text
Open questions:

- Should we use synchronous or asynchronous processing?
- How should we handle failures?
```

---

# 4. ADR（Architecture Decision Record）

高级工程师必须懂。

用途：

记录：

> 为什么当初这么设计。

---

很多公司系统几年后：

新人问：

为什么不用方案 B？

ADR 就是答案。

---

## ADR Template

```text
Title

Context

Decision

Alternatives Considered

Consequences
```

---

# Context

背景。

例如：

```text
The system needs to process millions of events daily.
```

---

# Decision

决定。

例如：

```text
We decided to adopt Kafka for event processing.
```

---

# Alternatives Considered

考虑过：

```text
Alternative solutions included RabbitMQ and database polling.
```

---

# Consequences

后果。

包括：

优点：

```text
Improved scalability.
```

缺点：

```text
Increased operational complexity.
```

---

# 5. API Documentation

开发者每天接触。

---

## API 文档结构：

```text
Endpoint

Method

Request

Response

Error Codes

Examples
```

---

例如：

## Endpoint

```text
GET /users/{id}
```

---

## Description

```text
Retrieves user information by ID.
```

---

## Request

```json
{
  "id": "123"
}
```

---

## Response

```json
{
  "name": "John"
}
```

---

## Error

```text
404 User not found

401 Unauthorized
```

---

注意：

API 文档喜欢：

retrieve

fetch

return

provide

---

# 6. README 写法

很多人低估 README。

好的 README 是工程入口。

---

结构：

```text
Overview

Features

Requirements

Installation

Configuration

Usage

Development

Troubleshooting
```

---

# Overview

```text
This project provides an authentication service for internal applications.
```

---

# Installation

```text
Run the following command:
```

---

# Configuration

```text
The service requires the following environment variables:
```

---

# Troubleshooting

解决问题：

```text
If you encounter connection errors, check your database configuration.
```

---

# 7. Incident Report / Postmortem

线上事故必备。

---

结构：

```text
Summary

Impact

Timeline

Root Cause

Resolution

Action Items
```

---

# Summary

```text
On July 10, the payment service experienced elevated error rates.
```

---

# Impact

重点：

影响谁。

```text
Approximately 20% of payment requests failed.
```

---

# Timeline

时间线。

```text
10:00 Deployment started.

10:15 Error rate increased.

10:30 Rollback completed.
```

---

# Root Cause

不要：

"The reason is..."

工程：

```text
The root cause was an incorrect configuration change.
```

---

# Action Items

后续：

```text
- Add configuration validation.
- Improve deployment checks.
- Add monitoring alerts.
```

---

# 8. 英文工程文档高频句型

这个非常值得背。

---

## 描述目的

```text
The goal of this document is to...
```

---

## 描述现状

```text
Currently, the system...
```

---

## 提出方案

```text
We propose to...
```

---

## 描述原因

```text
This is mainly due to...
```

---

## 描述影响

```text
This may impact...
```

---

## 描述限制

```text
One limitation of this approach is...
```

---

## 描述风险

```text
A potential risk is...
```

---

## 描述决定

```text
We decided to...
```

---

## 描述未来

```text
In the future, we plan to...
```

---

# 9. 中文开发文档 → 英文工程文档转换

---

中文：

> 为了解决数据库压力问题，我们增加缓存。

不要：

> To solve database pressure problem, we add cache.

工程：

```text
To address database load issues, we introduce a caching layer.
```

---

中文：

> 这个方案可能增加复杂度。

工程：

```text
This approach may introduce additional complexity.
```

---

中文：

> 我们选择方案 A，因为它更容易维护。

工程：

```text
We chose approach A because it provides better maintainability.
```

---

中文：

> 后续优化。

工程：

```text
Future improvements include...
```

---

# 10. Senior Engineer 最重要的文档能力

初级：

> 写代码。

中级：

> 写清楚代码。

高级：

> 写清楚为什么这么设计。

Staff：

> 写文档推动整个团队做正确决策。

---

# Part 25 核心总结

软件工程英文文档，本质是：

```text
Context
为什么

↓

Problem
问题

↓

Goal
目标

↓

Proposal
方案

↓

Trade-off
权衡

↓

Decision
决定

↓

Implementation
执行

↓

Result
结果
```

---

掌握 Part 25 后，你不仅能：

- 看懂英文技术文档
- 写 Jira
- 写 PR

还可以开始：

- 写 Design Doc
- 做 Architecture Review
- 参与英文技术讨论

---

下一部分如果继续，我建议做：

# Part 26：软件工程英文缩写与黑话大全（真实公司每天出现）

这个会补齐最后一块：

例如：

- LGTM
- WIP
- FYI
- ETA
- TBD
- ACK/NACK
- RFC
- MVP
- POC
- SLA
- SLO
- SLI
- MTTR
- DR
- CI/CD
- DX
- Tech Debt

这些不是技术词，但是英文工程团队沟通里出现频率极高。你现在前面的体系已经到了应该补这一块的时候。
