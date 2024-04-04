## 开发框架API
### 获取开发框架工具列表

> GET

- https://api.youyong.ba/development-frameworks

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
| title       | String  | 框架标题                           |
| icon        | String  | 框架图标链接                       |
| description | String  | 框架描述                           |
| id          | Number  | 框架ID                             |
| url         | String  | 框架链接                           |
| pinyin      | String  | 框架名称拼音                       |
| isTrending  | Boolean | 是否为热门框架                     |
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
      "thumbnail": "http://example.com/thumbnail13.jpg",
      "title": "全栈开发框架M",
      "icon": "http://example.com/icon13.png",
      "description": "支持多种编程语言和技术栈，提供一站式解决方案，帮助开发者快速搭建和部署高性能的应用程序。",
      "id": 13,
      "url": "http://example.com/frameworkM",
      "pinyin": "quanxiangaifakuangjia",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-01-05",
      "publisher": "开发者M"
    }
    // 此处可以根据实际情况添加更多框架项...
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
curl -X GET 'https://api.youyong.ba/development-frameworks?page=1&limit=10'
```