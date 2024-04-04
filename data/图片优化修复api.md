## 图片优化修复API
### 获取图片优化修复工具列表

> GET

- https://api.youyong.ba/image-repair-tools

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
      "thumbnail": "http://example.com/thumbnail2.jpg",
      "title": "图片优化修复工具B",
      "icon": "http://example.com/icon2.png",
      "description": "这是一个专注于图片质量优化和修复的工具，适用于各种常见的图片损坏问题。",
      "id": 2,
      "url": "http://example.com/toolB",
      "pinyin": "tupianyouhuaxiufu",
      "isTrending": true,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-02-01",
      "publisher": "开发者B"
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
curl -X GET 'https://api.youyong.ba/image-repair-tools?page=1&limit=10'
```









