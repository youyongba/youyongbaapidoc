## 图片插画生成API

### 获取图片插画生成工具列表

> GET

- https://api.youyong.ba/illustration-tools

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

```javascript
  {
    "page": 1,
    "limit": 10
  }
```

### 响应

#### 成功

```json
{
  "status": true,
  "message": "成功",
  "data": [
    {
      "thumbnail": "图像链接",
      "title": "工具名称",
      "icon": "图标链接",
      "description": "工具描述",
      "id": 1,
      "url": "工具网址",
      "pinyin": "工具名称的拼音",
      "isTrending": true,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "发布日期",
      "publisher": "发布者名称"
    }
    // 更多工具项...
  ]
}
```

#### 失败

```json
{
  "status": false,
  "message": "错误消息"
}
```

### 示例调用

```bash
curl -X GET 'http://api.example.com/illustration-tools?page=1&limit=10'
```

