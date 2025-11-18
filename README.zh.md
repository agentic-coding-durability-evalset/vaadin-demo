# Vaadin Demo

一个基于 [Vaadin](https://vaadin.com/) 和 [Spring Boot](https://spring.io/projects/spring-boot) 的 Java Web 应用示例项目。展示了如何使用 Vaadin 构建现代化的企业级 Web 应用。

## 技术栈

- **Java**: 21
- **Spring Boot**: 3.5.7
- **Vaadin**: 24.9.3
- **Spring Data JPA**: 数据访问层
- **H2 Database**: 内存数据库（开发环境）
- **Maven**: 构建工具

## 项目结构

```
vaadin-demo/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── org/mvnsearch/...       # Java 源代码
│   │   └── resources/
│   │       └── application.properties
│   └── test/             # 测试代码
├── pom.xml               # Maven 依赖配置
└── README.md
```

## 功能特性

- Vaadin 组件库
- Spring Boot 集成
- Spring Data JPA
- H2 数据库支持
- 响应式 UI
- 服务端渲染
- Actuator 监控端点

## 快速开始

### 前置要求

- Java 21 或更高版本
- Maven 3.6+

### 安装和运行

```bash

# 构建项目
mvn clean package

# 运行应用
mvn spring-boot:run
# 或
java -jar target/vaadin-demo-1.0-SNAPSHOT.jar
```

应用将在 `http://localhost:8080` 启动。

## 项目特点

### Vaadin 框架

Vaadin 是一个服务端驱动的 Web 框架：
- **服务端渲染**: UI 在服务器端生成
- **组件库**: 丰富的企业级组件
- **类型安全**: Java 类型安全的 UI 开发
- **自动通信**: 自动处理客户端-服务器通信

### Spring Boot 集成

- **自动配置**: Vaadin Spring Boot Starter
- **依赖注入**: Spring 的 DI 容器
- **数据访问**: Spring Data JPA
- **监控**: Spring Boot Actuator

### 视图开发

Vaadin 视图是普通的 Java 类：

```java
@Route("")
public class MainView extends VerticalLayout {
    public MainView() {
        add(new H1("Welcome to Vaadin"));
        add(new Button("Click me", e -> {
            Notification.show("Button clicked!");
        }));
    }
}
```


## 参考资源

- [Vaadin 官方网站](https://vaadin.com/)
- [Vaadin 文档](https://vaadin.com/docs)
- [Vaadin Spring Boot 集成](https://vaadin.com/docs/latest/integrations/spring/overview)
- [Vaadin 组件文档](https://vaadin.com/docs/latest/components)
