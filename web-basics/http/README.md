# HTTP 协议

> 浏览器和服务器对话的"语言"

## 是什么

**HTTP** (HyperText Transfer Protocol) = 超文本传输协议

它是**浏览器和服务器之间的通信规则**，规定了：
- 浏览器怎么向服务器"要东西"
- 服务器怎么"给东西"浏览器

## 为什么重要

所有 Web 开发都离不开 HTTP：
- 调 API、请求资源、处理登录...
- 面试必问：状态码、请求方法、缓存、HTTPS

## 怎么用

### 1. 请求组成

```
请求 = 请求行 + 请求头 + 请求体
```

**请求行示例：**
```
GET /api/users HTTP/1.1
```

**常见请求方法：**

| 方法 | 含义 | 典型场景 |
|------|------|----------|
| **GET** | 获取资源 | 访问页面、查询数据 |
| **POST** | 创建资源 | 提交表单、注册用户 |
| **PUT** | 更新资源 | 完整更新 |
| **DELETE** | 删除资源 | 删除数据 |
| **PATCH** | 部分更新 | 修改个别字段 |

### 2. 响应组成

```
响应 = 状态行 + 响应头 + 响应体
```

**状态行示例：**
```
HTTP/1.1 200 OK
```

**常见状态码：**

| 状态码 | 含义 | 说明 |
|--------|------|------|
| **200** | OK | 请求成功 |
| **201** | Created | 创建成功 |
| **400** | Bad Request | 请求参数错误 |
| **401** | Unauthorized | 未登录/未授权 |
| **403** | Forbidden | 没权限 |
| **404** | Not Found | 资源不存在 |
| **500** | Internal Server Error | 服务器内部错误 |

### 3. 请求头示例

```http
GET /api/user/1 HTTP/1.1
Host: api.example.com
Accept: application/json
Authorization: Bearer token123
User-Agent: Mozilla/5.0...
```

### 4. 响应体示例

```json
{
  "code": 200,
  "message": "success",
  "data": {
    "id": 1,
    "name": "张三",
    "email": "zhangsan@example.com"
  }
}
```

## 常见面试题

### Q: GET 和 POST 的区别？

| 区别 | GET | POST |
|------|-----|------|
| 用途 | 获取数据 | 提交数据 |
| 参数位置 | URL 查询参数 | 请求体 |
| 长度限制 | ~2KB | 无限制 |
| 缓存 | 可缓存 | 不可缓存 |
| 安全性 | 参数暴露 URL | 相对安全 |

### Q: HTTP 1.0 / 1.1 / 2.0 的区别？

- **HTTP 1.0**：每个请求单独 TCP 连接
- **HTTP 1.1**：**持久连接**（复用 TCP）、管道化
- **HTTP 2.0**：**多路复用**（并行请求）、头部压缩、Server Push

### Q: HTTPS 和 HTTP 的区别？

| 区别 | HTTP | HTTPS |
|------|------|-------|
| 安全性 | 明文传输 | SSL/TLS 加密 |
| 端口 | 80 | 443 |
| 证书 | 无 | 需要 CA 证书 |
| 性能 | 更快 | 略慢（加解密） |

---

## 下一步

- [RESTful API 设计](../restful-api/README.md)
- [Web 安全基础](../security/README.md)
