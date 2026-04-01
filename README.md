

# cn-weather-mcp

基于 Model Context Protocol (MCP) 的中国天气查询服务。这是一个 Spring Boot 应用程序，提供中国城市天气数据的查询功能。

## 功能特性

- **实时天气查询**：通过城市代码获取指定城市的当前天气信息
- **城市代码搜索**：根据城市名称搜索对应的天气代码
- **城市代码支持**：内置中国 300+ 城市代码数据

## 技术栈

- Java 17+
- Spring Boot 3.x
- Spring AI MCP (Model Context Protocol)
- Jackson JSON

## 快速开始

### 构建项目

```bash
./mvnw clean package
```

### 运行项目

```bash
./mvnw spring-boot:run
```

## 使用方法

本项目提供两个 MCP 工具：

### 1. 获取当前天气

根据城市代码查询天气信息。

**参数：**
- `cityCode`: 城市代码（如北京 101010100，上海 101020100）

**示例输入：**
```
101010100
```

### 2. 搜索城市代码

根据城市名称搜索对应的城市代码。

**参数：**
- `cityName`: 城市名称（如北京、上海、广州）

**示例输入：**
```
北京
```

## 城市代码参考

常见城市代码：

| 城市 | 代码 |
|------|------|
| 北京 | 101010100 |
| 上海 | 101020100 |
| 广州 | 101280101 |
| 深圳 | 101280601 |
| 杭州 | 101210101 |
| 成都 | 101270101 |
| 武汉 | 101200101 |
| 西安 | 101110101 |

## 配置说明

主要配置项在 `src/main/resources/application.yml` 中：

```yaml
spring:
  application:
    name: cn-weather-mcp
```

## 项目结构

```
cn-weather-mcp/
├── src/main/java/cn/wubo/cn/weather/mcp/
│   ├── WeatherApplication.java    # Spring Boot 启动类
│   └── WeatherService.java         # 天气服务核心类
├── src/main/resources/
│   └── application.yml             # 应用配置
└── pom.xml                         # Maven 依赖配置
```

## 许可证

MIT License