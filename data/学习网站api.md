## 学习网站API
### 获取学习网站列表

> GET

- https://api.youyong.ba/learning-sites

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
| title       | String  | 网站标题                           |
| icon        | String  | 网站图标链接                       |
| description | String  | 网站描述                           |
| id          | Number  | 网站ID                             |
| url         | String  | 网站链接                           |
| pinyin      | String  | 网站名称拼音                       |
| isTrending  | Boolean | 是否为热门网站                     |
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
      "thumbnail": "http://example.com/thumbnail12.jpg",
      "title": "终身学习平台L",
      "icon": "http://example.com/icon12.png",
      "description": "提供覆盖多个领域的在线课程和教程，包括编程、设计、市场营销等，帮助个人和团队实现职业发展和技能提升。",
      "id": 12,
      "url": "http://example.com/siteL",
      "pinyin": "zhongshenxuexipingtai",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-12-04",
      "publisher": "开发者L"
    }
    // 此处可以根据实际情况添加更多网站项...
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
curl -X GET 'https://api.youyong.ba/learning-sites?page=1&limit=10'
```