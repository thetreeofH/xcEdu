# 学成在线

## 1.项目介绍

当前市场的在线教育模式多种多样，包括：B2C、C2C、B2B2C等业务模式，学成在线采用B2B2C业务模式，即向 企业或个人提供在线教育平台提供教学服务，老师和学生通过平台完成整个教学和学习的过程

## 2.系统架构

![image-20210629172809100](C:\Users\yul\AppData\Roaming\Typora\typora-user-images\image-20210629172809100.png)

![image-20210629172851162](C:\Users\yul\AppData\Roaming\Typora\typora-user-images\image-20210629172851162.png)

### 业务流程举例：

1.  用户可以通过pc、手机等客户端访问系统进行在线学习。
2.   系统应用CDN技术，对一些图片、CSS、视频等资源从CDN调度访问。 
3. 所有的请求全部经过负载均衡器。 
4. 对于PC、H5等客户端请求，首先请求UI层，渲染用户界面
5. 客户端UI请求服务层获取进行具体的业务操作。 
6. 服务层将数据持久化到数据库。

## 3.技术栈

- 学成在线服务端基于Spring Boot构建，采用Spring Cloud微服务框架。
-  持久层：MySQL、MongoDB、Redis、ElasticSearch 
- 访问层：使用Spring Data JPA 、Mybatis、Spring Data Mongodb等 
- 业务层：Spring IOC、Aop事务控制、Spring Task任务调度、Feign、Ribbon、Spring AMQP、Spring Data Redis 等。
-  控制层：Spring MVC、FastJSON、RestTemplate、Spring Security Oauth2+JWT等 
- 微服务治理：Eureka、Zuul、Hystrix、Spring Cloud Config等