## 训练模型API
### 获取训练模型工具列表

> GET

- https://api.youyong.ba/training-model-tools

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
      "thumbnail": "http://example.com/thumbnail11.jpg",
      "title": "人工智能训练平台K",
      "icon": "http://example.com/icon11.png",
      "description": "提供全面的机器学习和深度学习模型训练服务，支持多种编程语言和框架，帮助开发者和研究人员快速构建和部署高效的AI模型。",
      "id": 11,
      "url": "http://example.com/toolK",
      "pinyin": "rengongzhinengxunlianpingtai",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2023-11-03",
      "publisher": "开发者K"
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
curl -X GET 'https://api.youyong.ba/training-model-tools?page=1&limit=10'
```