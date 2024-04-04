## 个人中心 -- 密码修改API
### 修改用户密码

> POST

- https://api.youyong.ba/user-profile/password-change

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

| 参数名          | 类型   | 描述       |
| -------------- | ------ | ---------- |
| currentPassword | String | 当前密码   |
| newPassword     | String | 新密码     |


```json
  {
    "currentPassword": "oldPassword123",
    "newPassword": "newPassword456"
  }
```


### 响应

#### 成功

```json
{
  "status": true,
  "message": "密码修改成功"
}
```

#### 失败

```json
{
  "status": false,
  "message": "当前密码不正确"
}
```

或

```json
{
  "status": false,
  "message": "新密码不符合安全要求"
}
```

### 示例调用

```bash
curl -X POST 'https://api.youyong.ba/user-profile/password-change' \
-H 'Authorization: Bearer xxx' \
-H 'Content-Type: application/json' \
-d '{
      "currentPassword": "oldPassword123",
      "newPassword": "newPassword456"
    }'
```