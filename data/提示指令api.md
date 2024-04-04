## 提示指令API
### 获取提示指令工具列表

> GET

- https://api.youyong.ba/prompting-tools

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
      "thumbnail": "http://example.com/thumbnail10.jpg",
      "title": "高级提示生成器J",
      "icon": "http://example.com/icon10.png",
      "description": "采用最新的人工智能技术，为用户提供高效、精准的写作和创作提示，支持多种语言和格式，适合各类创作者使用。",
      "id": 10,
      "url": "http://example.com/toolJ",
      "pinyin": "gaojitishengchengqi",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-10-02",
      "publisher": "开发者J"
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
curl -X GET 'https://api.youyong.ba/prompting-tools?page=1&limit=10'
```