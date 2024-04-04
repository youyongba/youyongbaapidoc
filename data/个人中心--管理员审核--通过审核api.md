个人中心 -- 管理员审核 -- 通过审核 API 设计如下：

### 通过待审核工具

> POST

- https://api.youyong.ba/admin/review-tools/approve

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

| 参数名 | 类型   | 描述         |
| ------ | ------ | ------------ |
| id     | number | 待审核工具ID |

```json
  {
    "id": 12345
  }
```

### 响应

#### 成功

```json
{
  "status": true,
  "message": "审核通过成功"
}
```

#### 失败

```json
{
  "status": false,
  "message": "审核失败，未找到对应的工具ID"
}
```

### 示例调用

```bash
curl -X POST 'https://api.youyong.ba/admin/review-tools/approve' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer xxx' \
-d '{"id": 12345}'
```
