# cn-weather-mcp

China weather query service based on Model Context Protocol (MCP).

<div align="right">
  English | <a href="README.zh-CN.md">中文</a>
</div>

## Features

- **Real-time weather query**: Get current weather information for a specified city through city code
- **City code search**: Search for corresponding weather codes based on city names, with built-in data of 300+ cities in China

## stdio configuration

> **Recommended**: No specific installation steps are needed when using jbang. We will use jbang to run cn-weather-mcp directly.

```json
{
  "mcpServers": {
    "cn-weather-mcp": {
      "args": [
        "io.github.wb04307201:cn-weather-mcp:1.0.0"
      ],
      "command": "jbang"
    }
  }
}
```

## Two tools provided:

### 1. Get current weather

Query weather information based on city code.

**Parameters:**
- `cityCode`: City code (e.g., Beijing 101010100, Shanghai 101020100)

**Example input:**
```
101010100
```

### 2. Search city code

Search for city code based on city name.

**Parameters:**
- `cityName`: City name (e.g., Beijing, Shanghai, Guangzhou)

**Example input:**
```
Beijing
```

## City code reference

Common city codes:

| City | Code        |
|------|-------------|
| Beijing | 101010100 |
| Shanghai | 101020100 |
| Guangzhou | 101280101 |
| Shenzhen | 101280601 |
| Hangzhou | 101210101 |
| Chengdu | 101270101 |
| Wuhan | 101200101 |
| Xi'an | 101110101 |