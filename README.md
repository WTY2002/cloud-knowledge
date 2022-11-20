# 云知社区

## 项目背景

## 项目模块

* 云知星球
* 云易购

## 技术选型

### 后端

<img src="http://rk8lx4oxj.hn-bkt.clouddn.com/image-20221120203251604.png" alt="image-20221120203251604" style="zoom:80%;" />

<img src="http://rk8lx4oxj.hn-bkt.clouddn.com/image-20221120203451858.png" alt="image-20221120203451858" style="zoom: 80%;" />

后端采用SpringCloud全家桶搭建微服务架构，相关技术选型如下：

* 权限控制框架+单点登录：Sa-Token
* 持久层框架：SpringData JPA
* 缓存：Redis
* 数据库连接池：Druid
* 微服务注册中心：Eureka

后在原本SpringCloud的基础上，换用了SpringCloud Alibaba相关中间件，使用Nacos作为微服务注册中心替换原本的Eureka，并根据业务的扩大，选择加入RabbitMQ和ElasticSearch技术

* 微服务注册中心：Nacos

* 接口文档：Knife4j
* 消息队列：RabbitMQ
* 搜索引擎：ElasticSearch

### 前端

<img src="http://rk8lx4oxj.hn-bkt.clouddn.com/image-20221120205004255.png" alt="image-20221120205004255" style="zoom: 50%;" />

* **云知星球**模块采用的是`vue.js`技术栈，使用的是`vue3 + typescript + pinia + vuerouter `
  ![image-20221120210439243](http://rk8lx4oxj.hn-bkt.clouddn.com/image-20221120210439243.png)
* **云易购**模块采用的是`React`技术栈，由于需要进行跨端开发，因此使用`React Native + React Navigation + TypeScript`，并结合`MeterialUI`组件库进行开发
  ![image-20221120210733811](http://rk8lx4oxj.hn-bkt.clouddn.com/image-20221120210733811.png)

## 开发情况

- [ ] 云知星球
- [ ] 云易购

## 运行手册

* 环境要求：
  * Java后台项目基础环境：`jdk8以上 + mysql5.7.x`
    * 数据库推荐修改为默认的：admin/123456
  * RabbitMQ环境：版本3.7.4
    * 用户名和密码为：admin/admin，不然需要修改项目的启动配置文件
  * 服务注册中心Nacos：2.1.2[Release 2.1.2 (Oct 17th, 2022) · alibaba/nacos (github.com)](https://github.com/alibaba/nacos/releases/tag/2.1.2)
* 运行方法：
  * 首先启动本机的Nacos和RabbitMQ服务
  * 然后再使用IDEA运行SpringBoot服务即可

