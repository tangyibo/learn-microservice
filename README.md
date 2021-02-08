
# 微服务组件

## 一、微服务概念

### 1、什么是微服务

微服务(Microservice Architecture) 是近几年流行的一种架构思想。是一种架构模式，或者说是一种架构风格，它体长将单一的应用程序划分成一组小的服务，每个服务运行在其独立的自己的进程内，服务之间互相协调，互相配置，为用户提供最终价值，服务之间采用轻量级的通信机制(HTTP)互相沟通，每个服务都围绕着具体的业务进行构建，并且能狗被独立的部署到生产环境中。

微服务化的核心就是将传统的一站式应用，根据业务拆分成一个一个的服务，彻底地去耦合，每一个微服务提供单个业务功能的服务，一个服务做一件事情，从技术角度看就是一种小而独立的处理过程，类似进程的概念，能够自行单独启动或销毁，拥有自己独立的数据库。

### 2、微服务优缺点

(1) 优点：

- 单一职责原则；
- 每个服务足够内聚，足够小，代码容易理解，这样能聚焦一个指定的业务功能或业务需求；
- `开发简单，开发效率高，一个服务可能就是专一的只干一件事`；
- 微服务能够被小团队单独开发，这个团队只需2-5个开发人员组成；
- 微服务是松耦合的，是有功能意义的服务，无论是在开发阶段或部署阶段都是独立的；
- 微服务能使用不同的语言开发；
- 易于和第三方集成，微服务允许容易且灵活的方式集成自动部署，通过持续集成工具，如jenkins，Hudson，bamboo；
- 微服务易于被一个开发人员理解，修改和维护，这样小团队能够更关注自己的工作成果，无需通过合作才能体现价值；
- 微服务允许利用和融合最新技术；
- 微服务只是业务逻辑的代码，不会和HTML，CSS，或其他的界面混合;
- 每个微服务都有自己的存储能力，可以有自己的数据库，也可以有统一的数据库；

(2) 缺点：

- 开发人员要处理分布式系统的复杂性；
- 多服务运维难度，随着服务的增加，运维的压力也在增大；
- 系统部署依赖问题；
- 服务间通信成本问题；
- 数据一致性问题；
- 系统集成测试问题；
- 性能和监控问题；

### 3、SpringCloud和SpringBoot的关系

- 1.SpringBoot专注于开苏方便的开发单个个体微服务；
- 2.SpringCloud是关注全局的微服务协调整理治理框架，它将SpringBoot开发的一个个单体微服务，整合并管理起来，为各个微服务之间提供：配置管理、服务发现、断路器、路由、代理、事件总线、全局锁、决策竞选、分布式会话等等集成服务；
- 3.SpringBoot可以离开SpringCloud独立使用，开发项目，但SpringCloud离不开SpringBoot，属于依赖关系；
- 4.SpringBoot专注于快速、方便的开发单个个体微服务，SpringCloud关注全局的服务治理框架；


## 二、微服务组件


[SpringCloud组件](https://img-blog.csdnimg.cn/20210131203220827.png)

注释：由于很多组件都不再维护了，Nacos取代了Eureka，Config，Bus组件，Nacos可以作为注册中心也可以作为配置中心，Feign服务间的远程调用被OpenFeign取代，Hystrix熔断降级限流被sentinel取代，Zuul网关被gateway网关取代，Ribbon目前还可以使用，以前的架构一般是：Eureka +Ribbon/Feign+Hystrix+Zuul+config+Bus+Stream；现在的架构：Nacos+OpenFeign/Ribbon+sentinel+gateway。

###  SpringBoot

###  分布式事务协调：Zookeeper

项目地址：https://github.com/apache/zookeeper

###  RPC通信：dubbo

项目地址：https://github.com/apache/dubbo

###  服务注册与配置管理：nacos

项目地址：https://github.com/alibaba/nacos

###  openfeign

项目地址：https://github.com/spring-cloud/spring-cloud-openfeign

###  客户端负载均衡：ribbon

项目地址：https://github.com/Netflix/ribbon/wiki/Getting-Started

###  路由网关：gateway

项目地址：https://github.com/spring-cloud/spring-cloud-gateway

###  限流熔断降级：sentinel

项目地址：https://github.com/alibaba/Sentinel

###  分布式事务：seata

项目地址：https://github.com/seata/seata

###  分布式锁：Redisson

项目地址：https://github.com/redisson/redisson

###  容器化部署：docker/k8s

项目地址：https://github.com/kubernetes/kubernetes
