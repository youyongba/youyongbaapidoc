## 图片插画生成API

### 获取图片插画生成工具列表

> GET

- https://api.youyong.ba/illustration-tools

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数

```javascript
  {
    "page": 1,
    "limit": 10
  }
```

### 响应

#### 成功



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
curl -X GET 'http://api.example.com/illustration-tools?page=1&limit=10'
```

