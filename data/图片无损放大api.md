### 获取图片无损放大工具列表

> GET

- https://api.youyong.ba/image-enhancement-tools

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

| 参数名 | 类型   | 描述     |
| ------ | ------ | -------- |
| page   | number | 页码     |
| limit  | number | 每页数量 |

```javascript 
  {
    "page": 1,
    "limit": 10
  }
```

### 响应

#### 成功

| 参数名        | 类型    | 描述           |
| ------------ | ------- | -------------- |
| thumbnail    | String  | 缩略图         |
| title        | String  | 工具标题       |
| icon         | String  | 工具图标       |
| description  | String  | 工具描述       |
| id           | Number  | 工具ID         |
| url          | String  | 工具链接       |
| pinyin       | String  | 工具名称拼音   |
| isTrending   | Boolean | 是否为热门工具   |
| isApproved   | Boolean | 是否通过审核     |
| isAdmin      | Boolean | 是否为管理员专用 |
| publishedAt  | String  | 发布日期       |
| publisher    | String  | 发布者         |

```json
{
  "status": true,
  "message": "成功",
  "data": [
      "thumbnail": "http://example.com/thumbnail1.jpg",
      "title": "无损放大工具A",
      "icon": "http://example.com/icon1.png",
      "description": "这是一个能够无损放大图片的工具，支持多种图片格式。",
      "id": 1,
      "url": "http://example.com/toolA",
      "pinyin": "wusunfangda",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-01-01",
      "publisher": "开发者A"
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
curl -X GET 'https://api.youyong.ba/image-enhancement-tools?page=1&limit=10'
```