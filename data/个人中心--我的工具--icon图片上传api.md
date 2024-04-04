## 个人中心 -- 我的工具 -- Icon图片上传API
### 上传工具Icon图片

> POST

- https://api.youyong.ba/my-tools/upload-icon

### header

```javascript
{
    "Authorization": "Bearer xxx",
    "Content-Type": "multipart/form-data"
}
```

### 参数

| 参数名 | 类型       | 描述           |
| ------ | ---------- | -------------- |
| icon   | File       | 工具Icon图片文件 |

### 响应

#### 成功

```json
{
  "status": true,
  "message": "Icon上传成功",
  "data": {
    "iconUrl": "http://example.com/path/to/uploaded/icon14.png"
  }
}
```

#### 失败

```json
{
  "status": false,
  "message": "Icon上传失败，[具体原因]"
}
```

### 示例调用

使用CURL上传文件时需要使用`-F`参数指定文件路径。以下示例展示了如何上传Icon图片：

```bash
curl -X POST 'https://api.youyong.ba/my-tools/upload-icon' \
-H 'Authorization: Bearer xxx' \
-F 'icon=@/path/to/icon14.png'
```

请注意，示例中的`@/path/to/icon14.png`需要替换为实际的文件路径。