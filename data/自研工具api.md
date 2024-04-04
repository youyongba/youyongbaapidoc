## 自研工具API
### 获取自研工具列表

> GET

- https://api.youyong.ba/self-developed-tools

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
      "thumbnail": "http://example.com/thumbnail14.jpg",
      "title": "创新编程辅助工具N",
      "icon": "http://example.com/icon14.png",
      "description": "结合最新技术研发的编程辅助工具，旨在提高开发效率，简化复杂编程任务，支持多种编程语言，适合初学者和资深开发者。",
      "id": 14,
      "url": "http://example.com/toolN",
      "pinyin": "chuangxinbianchengfuzhugongju",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2024-01-07",
      "publisher": "开发者N"
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
curl -X GET 'https://api.youyong.ba/self-developed-tools?page=1&limit=10'
```