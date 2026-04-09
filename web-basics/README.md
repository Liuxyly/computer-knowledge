# Web 开发基础知识

> 非网络专业也能看懂的 Web 入门指南

## 什么是 Web？

Web 就是**浏览器和服务器之间的通信**。

```
浏览器 (Client)  ←→  服务器 (Server)
```

- **浏览器**：你正在看网页的那个应用（Chrome、Edge、Safari）
- **服务器**：存放网页、数据的后台电脑

## 核心流程

```
1. 浏览器发起请求 → 服务器收到
2. 服务器处理请求（查数据库、执行逻辑）
3. 服务器返回响应 → 浏览器收到
4. 浏览器渲染页面（HTML/CSS/JS）
```

## 常见角色

| 角色 | 作用 |
|------|------|
| **前端** | 浏览器端，页面展示、交互 |
| **后端** | 服务器端，业务逻辑、数据处理 |
| **数据库** | 存储数据 |
| **API** | 前后端沟通的"桥梁" |

## Web 开发技术栈（主流）

| 层级 | 技术 |
|------|------|
| **前端** | HTML, CSS, JavaScript, Vue, React |
| **后端** | Java (Spring Boot), Python (Django/Flask), Node.js, Go |
| **数据库** | MySQL, PostgreSQL, Redis, MongoDB |
| **服务器** | Linux, Nginx, Docker |

## 你需要知道的

- **HTTP**：浏览器和服务器对话的"语言"
- **URL**：网址，访问资源的地址
- **JSON**：前后端传输数据的格式

---

## 下一步

- [HTTP 协议详解](./http/README.md)
- [RESTful API 设计](../restful-api/README.md)
