## 1️⃣ 日志系统（Logging System）✅

**这是我当时第一个提的**

包含的不是一句 `log.info`，而是整套：

* 日志门面：`SLF4J`
* 日志实现：`Logback / Log4j2`
* 统一日志格式（traceId、线程、类名）
* 按环境区分日志级别
* 异步日志
* 日志切分 / 归档
* （可选）ELK / Loki 对接

👉 脚手架价值：**你新项目不用再想日志怎么配**

---

## 2️⃣ 配置系统（Configuration System）

脚手架里一定要有：

* `application.yml` 分环境
* `dev / test / prod` profile
* 配置集中管理（可选）：

  * Nacos
  * Apollo
* 敏感配置隔离（密码、key）

👉 本质：**配置 ≠ 代码**

---

## 3️⃣ 异常 & 返回值系统（Error / Response System）🔥

这是很多脚手架**做得最差**的地方，但非常核心。

通常包括：

* 统一返回结构

  ```json
  { "code": 0, "msg": "ok", "data": {} }
  ```
* 全局异常处理（`@ControllerAdvice`）
* 业务异常 / 系统异常分层
* 错误码体系（不是直接 throw RuntimeException）

👉 没这个，你的 Controller 会迅速变成垃圾场

---

## 4️⃣ 鉴权 & 安全系统（Auth / Security System）

脚手架级别集成，而不是业务里乱写：

* 登录 / Token
* JWT / Sa-Token / Spring Security
* 用户上下文（当前用户是谁）
* 接口权限（RBAC）
* 接口白名单

👉 哪怕你现在不用，**脚手架也要预留扩展点**

---

## 5️⃣ 持久层系统（Persistence System）

一般包括：

* ORM 选型

  * MyBatis / MyBatis-Plus
  * JPA（少见但存在）
* 分页统一
* 逻辑删除
* 乐观锁
* SQL 日志控制

👉 这是“数据访问规范化”

---

## 6️⃣ 接口文档系统（API Doc System）

脚手架必备：

* Swagger / OpenAPI
* 自动扫描 Controller
* 统一注解规范
* 分环境开关（prod 禁用）

👉 没文档的脚手架 = 半成品

---

## 7️⃣ 参数校验系统（Validation System）

* `javax / jakarta validation`
* DTO 校验注解
* 校验失败统一返回
* 自定义校验器

👉 防止脏数据流进业务层

---

## 8️⃣ 链路追踪 / 上下文系统（Trace / Context）⭐

这也是你当时可能觉得我说“有点多”的地方：

* TraceId / RequestId
* MDC 绑定
* 日志、异常、调用链统一
  -（进阶）SkyWalking / Zipkin

👉 **不是为了炫技，是为了线上能排错**

---

## 9️⃣ 任务 & 调度系统（Scheduler）

* Spring Task / Quartz
* 分布式任务锁
* 失败重试
* 任务日志

---

## 10️⃣ 运维 & 监控系统（Ops / Observability）

脚手架级别集成：

* Actuator
* 健康检查
* 指标（Prometheus）
* 应用启动信息
