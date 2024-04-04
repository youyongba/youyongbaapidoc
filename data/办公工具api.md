## 办公工具API
### 获取办公工具列表

> GET

- https://api.youyong.ba/office-tools

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
      "thumbnail": "http://example.com/thumbnail7.jpg",
      "title": "智能办公助手G",
      "icon": "http://example.com/icon7.png",
      "description": "整合了日程管理、文件分享、会议调度等多项功能，提高工作效率，适用于各类办公场景。",
      "id": 7,
      "url": "http://example.com/toolG",
      "pinyin": "zhinengbangongzhushou",
      "isTrending": true,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-07-30",
      "publisher": "开发者G"
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
curl -X GET 'https://api.youyong.ba/office-tools?page=1&limit=10'
```