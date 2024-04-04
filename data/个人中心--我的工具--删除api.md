## 个人中心 -- 我的工具 -- 删除API
### 删除已有的自研工具

> POST

- https://api.youyong.ba/my-tools/delete

### header

```javascript
{
    "Authorization": "Bearer xxx",
    "Content-Type": "application/json"
}
```

### 参数

| 参数名 | 类型   | 描述     |
| ------ | ------ | -------- |
| id     | Number | 工具ID   |


```json
{
  "id": 14
}
```

### 响应

#### 成功

```json
{
  "status": true,
  "message": "工具删除成功"
}
```

#### 失败

```json
{
  "status": false,
  "message": "删除工具失败，[具体原因]"
}
```

### 示例调用

```bash
curl -X DELETE 'https://api.youyong.ba/my-tools/delete' \
-H 'Authorization: Bearer xxx' \
-H 'Content-Type: application/json' \
-d '{"id": 14}'
```