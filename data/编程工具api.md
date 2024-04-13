## 编程工具API
### 获取编程工具列表

> GET

- https://api.youyong.ba/programming-tools

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
    "data": {
      "list":[
      {
        "thumbnail": "247.5*116",
        "title": "chatgpt",
        "icon": "xxx.png",
        "description": "chatgpt是一个开源的聊天机器人项目，基于GPT-3模型，可以实现自然语言对话和文本生成。",
        "id": 1,
        "url": "http://chatgpt.com",
        "pinyin": "chatgpt",
        "publishedAt": "2021-01-01",
        "publisher": "张三"
      }
      // 可能包含更多工具项...
    ],
    "total": 100
    }
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
curl -X GET 'https://api.youyong.ba/programming-tools?page=1&limit=10'
```



