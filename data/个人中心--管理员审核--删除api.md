个人中心 -- 管理员审核 -- 删除 API 设计如下：

### 删除待审核工具

> DELETE

- https://api.youyong.ba/admin/review-tools/delete

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

| 参数名 | 类型   | 描述       |
| ------ | ------ | ---------- |
| id     | number | 待删除工具ID |

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
  "message": "删除成功"
}
```

#### 失败

```json
{
  "status": false,
  "message": "删除失败，未找到对应的工具ID"
}
```

### 示例调用

```bash
curl -X DELETE 'https://api.youyong.ba/admin/review-tools/delete' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer xxx' \
-d '{"id": 12345}'
```
