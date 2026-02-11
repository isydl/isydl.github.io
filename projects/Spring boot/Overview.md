功能块 1：启动与阶段（Startup & Phases）【最高优先级】

你要解决的问题：

程序从哪一行开始“进入 Spring”

启动被切成了哪几个阶段

每个阶段有哪些可插点

只读这些关键词：

SpringApplication

run()

Application Events

ApplicationListener

📌 读到“能画出启动阶段分段图”为止，立刻停

功能块 2：自动配置机制（Auto Configuration）【最高优先级】

你要解决的问题：

Bean 是怎么“自动冒出来的”

Starter 为什么不用配就能用

只读这些关键词：

@SpringBootApplication

@EnableAutoConfiguration

AutoConfigurationImportSelector

条件注解（OnClass / OnBean / OnMissingBean）

📌 不要深入任何具体 Starter

功能块 3：容器刷新与 Bean 生命周期（Context & Bean）

你要解决的问题：

Bean 什么时候被“看见”

Bean 什么时候能被修改

只关心：

ApplicationContext.refresh

BeanFactoryPostProcessor

BeanPostProcessor

📌 这里不是背 API，是知道“在哪个阶段能干预”

功能块 4：配置与环境（Config & Environment）

你要解决的问题：

application.yml 在哪被加载

Profile、生效顺序

只关心：

Environment

PropertySource 顺序

外部化配置加载时机

📌 看懂一次即可，后续按需回查

功能块 5：启动完成后的扩展点（Post Startup）

你要解决的问题：

启动后我能干嘛

Runner、ReadyEvent 的区别

关键词：

ApplicationRunner

CommandLineRunner

ApplicationReadyEvent

功能块 6：失败与关闭（Failure & Shutdown）

你要解决的问题：

启动失败发生在哪

资源什么时候释放

只看：

ApplicationFailedEvent

Shutdown hook