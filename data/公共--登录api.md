## 公共 -- 登录API
### 用户登录

> POST

- https://api.youyong.ba/public-login

### header

```javascript
{
    "Content-Type": "application/json"
}
```

### 参数
> 用户名是经过加密后的,后端是需要解密的

| 参数名     | 类型   | 描述       |
| ---------- | ------ | ---------- |
| username   | String | 用户名     |
| password   | String | 密码       |


```json
  {
    "username": "userExample",
    "password": "password123"
  }
```

### 响应

#### 成功

```json
{
  "status": true,
  "message": "登录成功",
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX2lkIjoxLCJ1c2VybmFtZSI6InVzZXJFeGFtcGxlIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c",
    "userId": 1,
    "username": "userExample"
  }
}
```

#### 失败

```json
{
  "status": false,
  "message": "用户名或密码错误"
}
```

### 示例调用

```bash
curl -X POST 'https://api.youyong.ba/public-login' \
-H 'Content-Type: application/json' \
-d '{
      "username": "userExample",
      "password": "password123"
    }'
```