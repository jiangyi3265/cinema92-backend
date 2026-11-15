# cinema92-backend

基于若依的 Java 后端基础工程，为 cinema92-admin 提供管理 API，供 cinema92-app 后续接入。

## 项目简介

目前包含用户、角色、菜单、部门、字典、参数、公告和登录鉴权等若依基础模块。尚未实现演出、选座、预约订单及核销业务。仓库含定时任务和代码生成模块源码，但入口模块已注释其依赖。

## 技术栈

Java 8、Maven、Spring Boot 2.5.15、Spring Security、MyBatis、MySQL、Redis、Druid、JWT。

## 关联仓库

| 项目 | 说明 | GitHub |
| --- | --- | --- |
| cinema92-backend | 后端服务 | [cinema92-backend](https://github.com/jiangyi3265/cinema92-backend) |
| cinema92-admin | 管理后台 | [cinema92-admin](https://github.com/jiangyi3265/cinema92-admin) |
| cinema92-app | 用户端基础模板 | [cinema92-app](https://github.com/jiangyi3265/cinema92-app) |

## 快速启动

安装 JDK 8、Maven、MySQL 和 Redis。将 resources 下两个 application*.example.yml 复制为对应 application*.yml，设置 DB_URL、DB_USERNAME、DB_PASSWORD、REDIS_PASSWORD、JWT_SECRET、DRUID_PASSWORD 环境变量。数据库原始 SQL 因含账号初始化数据保留本地而不公开，需由维护者提供并初始化后启动。

```bash
mvn clean package -DskipTests
java -jar ruoyi-admin/target/ruoyi-admin.jar
```
默认端口 8080。不要将生成的本地配置提交。

## 项目结构

- `ruoyi-admin/`：启动入口与控制器
- `ruoyi-framework/`：认证、安全和框架配置
- `ruoyi-system/`：系统业务与 Mapper
- `ruoyi-common/`：公共工具及模型
- `ruoyi-generator/`、`ruoyi-quartz/`：保留的可选模块源码
- `sql/`：本地初始化资料（未公开）

## 简历描述示例

以下描述仅适用于实际参与相关工作时，不代表已完成规划功能。

维护基于 Spring Boot 和 MyBatis 的管理后台基础服务，理解用户权限、JWT 鉴权与多模块工程组织，为演出预约业务提供后续扩展基础。

## 配置与许可证

本地环境文件、凭据、数据库数据、依赖及构建产物不公开。保留原有许可证与上游归属；后端和管理端基于若依项目。
