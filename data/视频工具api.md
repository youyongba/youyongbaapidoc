## 视频工具API
### 获取视频工具列表

> GET

- https://api.youyong.ba/video-tools

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


```json
  {
    "page": 1,
    "limit": 10
  }
```


### 响应

#### 成功


| 参数名       | 类型    | 描述                               |
| ----------- | ------- | ---------------------------------- |
| thumbnail   | String  | 缩略图链接                         |
| title       | String  | 工具标题                           |
| icon        | String  | 工具图标链接                       |
| description | String  | 工具描述                           |
| id          | Number  | 工具ID                             |
| url         | String  | 工具链接                           |
| pinyin      | String  | 工具名称拼音                       |
| isTrending  | Boolean | 是否为热门工具                     |
| isApproved  | Boolean | 是否通过审核                       |
| isAdmin     | Boolean | 是否为管理员专用                   |
| publishedAt | String  | 发布日期                           |
| publisher   | String  | 发布者                             |


```json
{
  "status": true,
  "message": "成功",
  "data": [
    {
      "thumbnail": "http://example.com/thumbnail3.jpg",
      "title": "视频编辑工具C",
      "icon": "http://example.com/icon3.png",
      "description": "提供全面的视频编辑功能，包括剪辑、合并、特效等，适合所有级别的用户。",
      "id": 3,
      "url": "http://example.com/toolC",
      "pinyin": "shipinbianjigongju",
      "isTrending": true,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-03-10",
      "publisher": "开发者C"
    }
    // 此处可以根据实际情况添加更多工具项...
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
curl -X GET 'https://api.youyong.ba/video-tools?page=1&limit=10'
```