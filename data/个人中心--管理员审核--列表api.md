## 个人中心 -- 管理员审核 -- 列表API
### 获取待审核工具列表

> GET

- https://api.youyong.ba/admin/review-tools/list

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
| isApproved  | Boolean | 审核状态                           |
| isAdmin     | Boolean | 是否为管理员专用                   |
| publishedAt | String  | 发布日期                           |
| publisher   | String  | 发布者                             |
| categoryType   | String  | 工具类别                           |


```json
{
  "status": true,
  "message": "成功",
  "data": [
    {
      "thumbnail": "待审核工具缩略图链接",
      "title": "待审核工具标题",
      "icon": "待审核工具图标链接",
      "description": "待审核工具描述",
      "id": "待审核工具ID",
      "url": "待审核工具链接",
      "pinyin": "待审核工具名称拼音",
      "categoryType":"待审核工具类别",
      "isTrending": false,
      "isApproved": false,
      "isAdmin": true,
      "publishedAt": "待审核工具发布日期",
      "publisher": "管理员"
    }
    // 此处可以根据实际情况添加更多待审核工具项...
  ]
}
```

#### 失败

```json
{
  "status": false,
  "message": "获取列表失败"
}
```

### 示例调用

```bash
curl -X GET 'https://api.youyong.ba/admin/review-tools/list?page=1&limit=10' \
-H 'Authorization: Bearer xxx'
```