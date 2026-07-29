> Pulse 会有的哪些文档

---

# Pulse 项目文档体系（v1.0）

## 1. 项目启动阶段（Project Initiation）

| 文档                                                                    | 语言 | 用途                                    |
| ----------------------------------------------------------------------- | ---- | --------------------------------------- |
| [Project Overview](/articles/documentation/Pulse/Project%20Overview.md) | 英语 | 介绍项目目的、技术定位，给开发团队看    |
| Product Vision（产品愿景）                                              | 日语 | 模拟日本客户/业务方说明为什么做这个系统 |
| Stakeholder List（相关人员列表）                                        | 日语 | 记录客户、管理员、开发负责人等角色      |

---

# 2. 需求分析阶段（Requirements）

这是最适合练日语的阶段。

| 文档                                                                        | 语言 | 用途                 |
| --------------------------------------------------------------------------- | ---- | -------------------- |
| 要件定義書（Requirements Specification）                                    | 日语 | 模拟日本客户需求文档 |
| [機能一覧](/articles/documentation/Pulse/Feature%20List.md)（Feature List） | 日语 | 列出系统功能         |
| 画面仕様書（Screen Specification）                                          | 日语 | 页面需求说明         |
| 業務フロー（Business Flow）                                                 | 日语 | 描述业务流程         |
| ユーザーシナリオ（User Scenario）                                           | 日语 | 用户如何使用系统     |

例如：

```
ユーザーが問い合わせを登録する。
担当者が対応状況を更新する。
管理者が完了確認を行う。
```

这些属于日本项目非常常见的文档。

---

# 3. 基本设计阶段（High Level Design）

这里开始英语增加。

| 文档                       | 语言 | 用途         |
| -------------------------- | ---- | ------------ |
| System Architecture Design | 英语 | 系统架构设计 |
| Database Design            | 英语 | 数据库设计   |
| API Specification          | 英语 | 接口设计     |
| Security Design            | 英语 | 安全设计     |
| Permission Design          | 英语 | 权限设计     |

原因：

这些属于开发团队内部技术文档。

---

# 4. 详细设计阶段（Low Level Design）

| 文档                      | 语言 | 用途         |
| ------------------------- | ---- | ------------ |
| Class Design              | 英语 | 类设计       |
| Sequence Diagram          | 英语 | 时序设计     |
| ER Diagram                | 英语 | 数据库关系   |
| Interface Design          | 英语 | 接口详细说明 |
| Exception Handling Design | 英语 | 异常处理设计 |

---

# 5. 开发阶段（Implementation）

| 文档                 | 语言 | 用途     |
| -------------------- | ---- | -------- |
| Source Code          | 英语 | 代码本身 |
| Git Commit Message   | 英语 | 提交记录 |
| Code Review Comments | 英语 | 代码评审 |
| Technical Notes      | 英语 | 技术记录 |

例如：

Git：

```
Add ticket creation API

Fix status transition validation
```

---

# 6. 测试阶段（Testing）

这里日语和英语都有。

## 面向业务测试：

| 文档                         | 语言 |
| ---------------------------- | ---- |
| テスト仕様書（测试规格书）   | 日语 |
| 受入テスト仕様書（验收测试） | 日语 |
| 操作確認書（操作确认）       | 日语 |

因为日本客户会看。

---

## 面向开发测试：

| 文档                    | 语言 |
| ----------------------- | ---- |
| Unit Test Specification | 英语 |
| API Test Report         | 英语 |
| Performance Test Report | 英语 |

---

# 7. 发布阶段（Release）

| 文档               | 语言 | 用途             |
| ------------------ | ---- | ---------------- |
| Release Notes      | 英语 | 开发团队版本记录 |
| Deployment Guide   | 英语 | 部署说明         |
| 運用手順書         | 日语 | 客户运维手册     |
| ユーザーマニュアル | 日语 | 用户使用说明     |

---

# 8. 维护阶段（Maintenance）

| 文档                     | 语言      |
| ------------------------ | --------- |
| 障害報告書（Bug Report） | 日语      |
| Incident Report          | 英语      |
| Change Request           | 英语/日语 |
| 改修仕様書               | 日语      |
| Technical Investigation  | 英语      |

---

# 最终你的仓库文档建议

```text
Pulse/

docs/

├── ja/
│
│── 01_requirements/
│   ├── 要件定義書.md
│   ├── 機能一覧.md
│   ├── 業務フロー.md
│   └── 画面仕様書.md
│
│── 02_test/
│   ├── テスト仕様書.md
│   └── 受入テスト.md
│
│── 03_operation/
│   ├── ユーザーマニュアル.md
│   └── 運用手順書.md
│
└── en/
│
│── 01_design/
│   ├── architecture.md
│   ├── database-design.md
│   └── api-specification.md
│
│── 02_development/
│   ├── development-guide.md
│   └── coding-standard.md
│
│── 03_release/
    ├── deployment-guide.md
    └── release-notes.md
```

---

日语重点：

> 要件定義 → 業務フロー → 画面仕様 → テスト → 操作マニュアル → 障害報告

英语重点：

> Architecture → Database → API → Code → Review → Deployment
