## 语言翻译API
### 获取语言翻译工具列表

> GET

- https://api.youyong.ba/translation-tools

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
      "thumbnail": "http://example.com/thumbnail8.jpg",
      "title": "全球语言翻译工具H",
      "icon": "http://example.com/icon8.png",
      "description": "支持多种语言互译，界面友好，翻译准确率高，适合个人和企业使用，帮助跨越语言障碍。",
      "id": 8,
      "url": "http://example.com/toolH",
      "pinyin": "quanguoyuyanfanyigongju",
      "isTrending": true,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-08-15",
      "publisher": "开发者H"
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
curl -X GET 'https://api.youyong.ba/translation-tools?page=1&limit=10'
```