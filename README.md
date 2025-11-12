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
│   │   │   └── ...       # Java 源代码
│   │   │       ├── views/ # Vaadin 视图
│   │   │       ├── services/ # 业务逻辑
│   │   │       └── entities/ # JPA 实体
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
# 克隆项目
git clone <repository-url>
cd vaadin-demo

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

## 开发

### 创建新视图

1. 创建继承 `VerticalLayout` 或其他布局的类
2. 使用 `@Route` 注解定义路由
3. 在构造函数中构建 UI

### 数据绑定

Vaadin 支持数据绑定：

```java
Binder<Person> binder = new Binder<>(Person.class);
TextField nameField = new TextField("Name");
binder.bind(nameField, Person::getName, Person::setName);
```

### 主题定制

可以自定义主题和样式：
- CSS 文件
- Lumo 主题变量
- 自定义组件样式

## 数据库

### H2 数据库

默认使用 H2 内存数据库（开发环境）：
- 无需额外配置
- 自动创建表结构
- 适合快速开发

### 生产数据库

可以配置 MySQL、PostgreSQL 等：

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=user
spring.datasource.password=password
```

## 构建和部署

### 生产构建

```bash
# 构建生产版本
mvn clean package -Pproduction
```

生产构建会：
- 优化前端资源
- 压缩 JavaScript
- 生成静态资源

### 部署选项

- **JAR 文件**: 独立可执行 JAR
- **WAR 文件**: 部署到应用服务器
- **Docker**: 容器化部署
- **云平台**: 各种云服务

## 参考资源

- [Vaadin 官方网站](https://vaadin.com/)
- [Vaadin 文档](https://vaadin.com/docs)
- [Vaadin Spring Boot 集成](https://vaadin.com/docs/latest/integrations/spring/overview)
- [Vaadin 组件文档](https://vaadin.com/docs/latest/components)
