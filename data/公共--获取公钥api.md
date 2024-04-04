## 公共 -- 获取公钥API
### 获取服务器公钥

> GET

- https://api.youyong.ba/public-key

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

无需参数

### 响应

#### 成功

```json
{
  "status": true,
  "message": "成功",
  "data": {
    "publicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAn3+Qk6MVZ2+3YRZS2Zsj..."
  }
}
```

#### 失败

```json
{
  "status": false,
  "message": "无法获取公钥"
}
```

### 示例调用

```bash
curl -X GET 'https://api.youyong.ba/public-key' \
-H 'Authorization: Bearer xxx'
```