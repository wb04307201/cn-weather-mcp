# cn-weather-mcp

A China weather query service based on the Model Context Protocol (MCP). This is a Spring Boot application providing weather data lookup for Chinese cities.

## Features

- **Real-time Weather Query**: Retrieve current weather information for a specified city using its city code
- **City Code Search**: Search for the corresponding weather code by city name
- **City Code Support**: Built-in data for 300+ Chinese city codes

## Technology Stack

- Java 17+
- Spring Boot 3.x
- Spring AI MCP (Model Context Protocol)
- Jackson JSON

## Quick Start

### Build the Project

```bash
./mvnw clean package
```

### Run the Project

```bash
./mvnw spring-boot:run
```

## Usage

This project provides two MCP tools:

### 1. Get Current Weather

Query weather information using a city code.

**Parameters:**
- `cityCode`: City code (e.g., Beijing: 101010100, Shanghai: 101020100)

**Example Input:**
```
101010100
```

### 2. Search City Code

Search for the city code by city name.

**Parameters:**
- `cityName`: City name (e.g., Beijing, Shanghai, Guangzhou)

**Example Input:**
```
Beijing
```

## City Code Reference

Common city codes:

| City | Code |
|------|------|
| Beijing | 101010100 |
| Shanghai | 101020100 |
| Guangzhou | 101280101 |
| Shenzhen | 101280601 |
| Hangzhou | 101210101 |
| Chengdu | 101270101 |
| Wuhan | 101200101 |
| Xi'an | 101110101 |

## Configuration

Main configuration is located in `src/main/resources/application.yml`:

```yaml
spring:
  application:
    name: cn-weather-mcp
```

## Project Structure

```
cn-weather-mcp/
├── src/main/java/cn/wubo/cn/weather/mcp/
│   ├── WeatherApplication.java    # Spring Boot main class
│   └── WeatherService.java         # Core weather service class
├── src/main/resources/
│   └── application.yml             # Application configuration
└── pom.xml                         # Maven dependency configuration
```

## License

MIT License