个人中心 -- 管理员审核 -- 不通过审核 API 设计如下：

### 审核不通过待审核工具

> POST

- https://api.youyong.ba/admin/review-tools/reject

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

| 参数名  | 类型   | 描述             |
| ------- | ------ | ---------------- |
| id      | number | 待审核工具ID     |
| reason  | string | 不通过审核的原因 |

```json
  {
    "id": 12345,
    "reason": "不满足审核标准"
  }
```

### 响应

#### 成功

```json
{
  "status": true,
  "message": "审核不通过成功"
}
```

#### 失败

```json
{
  "status": false,
  "message": "审核不通过失败，未找到对应的工具ID"
}
```

### 示例调用

```bash
curl -X POST 'https://api.youyong.ba/admin/review-tools/reject' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer xxx' \
-d '{"id": 12345, "reason": "不满足审核标准"}'
```

这段API文档定义了管理员如何执行审核不通过的操作，允许管理员明确指出不通过审核的具体原因。通过在请求体中提供待审核工具的ID和不通过的原因，管理员可以具体地指出每个工具不通过审核的具体理由。成功和失败的响应确保了管理员能够清晰地了解到操作的结果和状态。