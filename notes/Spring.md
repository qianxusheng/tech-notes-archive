https://spring.io/projects/spring-framework
---
- Spring IOC (Inversion of Control): 理解 Spring 的控制反转思想，学习如何通过 Spring 容器管理对象的生命周期、依赖注入和解耦。
- Dependency Injection (DI): 学习依赖注入的基本原理和方式，包括构造器注入、Setter 注入和接口注入等。
- Spring AOP (Aspect-Oriented Programming): 学习面向切面编程，如何在 Spring 中实现横切关注点（如日志、事务管理等）和分离关注点的功能。
- Spring MVC: 学习基于 MVC（Model-View-Controller）设计模式的 Web 开发，了解控制器、视图解析器、请求映射、拦截器等概念。
- Spring Boot: 学习如何使用 Spring Boot 简化应用程序的开发，自动化配置，嵌入式服务器和快速开发等。
- Spring Data: 学习如何使用 Spring Data 简化与数据库的交互，支持 JPA（Java Persistence API）、MongoDB、Redis 等数据库访问。
- Spring Security: 学习如何在应用中集成安全管理，包括身份验证、授权和加密等。
- Spring Transaction Management: 学习如何使用 Spring 提供的事务管理功能，支持声明式事务和编程式事务。
- Spring Cloud: 如果涉及到微服务架构，可以学习 Spring Cloud 相关组件，如 Eureka、Ribbon、Hystrix 等。
- Spring Test: 学习如何使用 Spring Test 模块进行单元测试和集成测试。
# Spring 框架学习路径

## 1. 基础知识
- **IoC（控制反转）**：理解 Spring 容器的作用和依赖注入的概念。学习如何通过配置文件或注解来管理 Bean。
- **AOP（面向切面编程）**：掌握 AOP 的核心概念，理解如何通过 AOP 来做日志、权限控制、事务管理等。

## 2. Spring 核心概念
- **Bean 和容器**：学习什么是 Spring Bean，如何配置和管理 Bean（包括注解方式和 XML 配置方式）。了解 Spring 容器是如何工作的。
- **注解**：
  - `@Component`：定义一个通用的 Spring Bean。
  - `@Service`、`@Repository`：分别用于标识服务层和数据访问层的 Bean。
  - `@Autowired`：自动注入 Bean。

## 3. Bean 生命周期
- 了解 Bean 的生命周期：从创建到销毁的过程，包括初始化、依赖注入、销毁等。

## 4. Spring AOP
- 学习如何使用 Spring AOP 来实现日志记录、权限验证、事务管理等横切关注点。

## 5. Spring MVC（Web 层开发）
- **DispatcherServlet 工作流程**：理解 Spring MVC 请求处理流程，从接收请求到返回响应。
- **Controller、RequestMapping、ModelAndView**：掌握如何编写控制器、使用请求映射注解来处理请求，理解 ModelAndView 的使用。

## 6. 前后端数据交互
- **Json**：了解如何通过 `@ResponseBody` 进行 JSON 数据的返回。
- **Form、PathVariable**：学习通过表单提交数据和使用路径变量获取数据。

## 7. Spring 与数据库整合
- **JdbcTemplate 使用**：了解如何使用 JdbcTemplate 来操作数据库。
- **Spring + MyBatis / JPA**：学习如何整合 MyBatis 或 JPA 与 Spring 进行数据库操作。

## 8. 声明式事务管理
- 了解 `@Transactional` 注解的使用，学习如何通过声明式事务管理来确保事务的一致性。

## 9. Spring Boot（推荐同时学习）
- **快速搭建项目**：学习如何快速创建和配置 Spring Boot 项目，理解自动配置的概念。
- **配置文件（application.yml）**：了解如何通过配置文件进行配置，掌握常见的配置项。
- **内嵌 Tomcat 启动**：理解 Spring Boot 如何自动配置 Tomcat 并通过内嵌方式启动。
