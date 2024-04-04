
## 音频工具 API

### 获取音频工具列表

> get

- https://api.youyongba.com/audio

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

| 参数名 | 类型   | 描述     |
| ------ | ------ | -------- |
| thumbnail   | String | 缩略图 |
| title  | number | 每页数量 |
| icon  | number | 每页数量 |
| description  | number | 每页数量 |
| id  | number | 每页数量 |
| url  | number | 每页数量 |
| pinyin  | number | 每页数量 |
| publishedAt  | number | 每页数量 |
| publisher  | number | 每页数量 |

  ```json
  {
    "status": true,
    "message": "成功",
    "data": [
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


#### 示例调用

使用 cURL 进行 API 调用的示例：

```bash
curl -X GET 'https://api.youyongba.com/audio?page=1&limit=10'
```


