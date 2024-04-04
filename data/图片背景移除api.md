## 图片背景移除API

### 获取图片背景移除工具列表

> GET

- https://api.youyong.ba/background-removal-tools

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

| 参数名       | 类型    | 描述                             |
| ----------- | ------- | -------------------------------- |
| thumbnail   | String  | 工具的缩略图链接                 |
| title       | String  | 工具的名称                       |
| icon        | String  | 工具的图标链接                   |
| description | String  | 对工具的描述                     |
| id          | Number  | 工具的唯一标识符                 |
| url         | String  | 工具的网址                       |
| pinyin      | String  | 工具名称的拼音，便于查找和排序   |
| isTrending  | Boolean | 表示工具是否处于热门状态         |
| isApproved  | Boolean | 工具是否已经通过审核             |
| isAdmin     | Boolean | 是否为管理员专用工具             |
| publishedAt | String  | 工具发布的日期                   |
| publisher   | String  | 工具的发布者名称                 |

```json
{
  "status": true,
  "message": "成功",
  "data": [
    {
      "thumbnail": "图像链接",
      "title": "工具名称",
      "icon": "图标链接",
      "description": "工具描述",
      "id": 1,
      "url": "工具网址",
      "pinyin": "工具名称的拼音",
      "isTrending": true,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "发布日期",
      "publisher": "发布者名称"
    }
    // 更多工具项...
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
curl -X GET 'http://api.example.com/background-removal-tools?page=1&limit=10'
```





