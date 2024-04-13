## 个人中心 -- 我的工具 -- 列表API
### 获取用户自己的工具列表

> GET

- https://api.youyong.ba/my-tools/list

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
| categoryType   | String  | 用户工具类别                             |



```json
{
  "status": true,
  "message": "成功",
  "data": {

    "list":  [
    {
      "thumbnail": "用户工具缩略图链接",
      "title": "用户工具标题",
      "icon": "用户工具图标链接",
      "description": "用户工具描述",
      "id": "用户工具ID",
      "url": "用户工具链接",
      "pinyin": "用户工具名称拼音",
      "categoryType":"用户工具类别",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "用户工具发布日期",
      "publisher": "用户"
    }
    // 此处可以根据实际情况添加更多用户工具项...
  ],
  "total": 100
  }
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
curl -X GET 'https://api.youyong.ba/my-tools/list?page=1&limit=10' \
-H 'Authorization: Bearer xxx'
```