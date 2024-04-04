## 个人中心 -- 我的工具 -- 缩略图图片上传API
### 上传工具缩略图图片

> POST

- https://api.youyong.ba/my-tools/upload-thumbnail

### header

```javascript
{
    "Authorization": "Bearer xxx",
    "Content-Type": "multipart/form-data"
}
```

### 参数

| 参数名    | 类型  | 描述               |
| --------- | ----- | ------------------ |
| thumbnail | File  | 工具缩略图图片文件 |

### 响应

#### 成功

```json
{
  "status": true,
  "message": "缩略图上传成功",
  "data": {
    "thumbnailUrl": "http://example.com/path/to/uploaded/thumbnail14.jpg"
  }
}
```

#### 失败

```json
{
  "status": false,
  "message": "缩略图上传失败，[具体原因]"
}
```

### 示例调用

使用CURL上传文件时需要使用`-F`参数指定文件路径。以下示例展示了如何上传缩略图图片：

```bash
curl -X POST 'https://api.youyong.ba/my-tools/upload-thumbnail' \
-H 'Authorization: Bearer xxx' \
-F 'thumbnail=@/path/to/thumbnail14.jpg'
```

请注意，示例中的`@/path/to/thumbnail14.jpg`需要替换为实际的文件路径。