
# 热门工具 API

## 获取热门工具列表

> get

- https://api.youyongba.com/pt

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```


### 参数
> `application/json`

> 无需在 URL 中传递参数。 黑认是page=1, limit=10


字段 | 类型  | 说明
:--- | :--- | :---
page | Number | 第几页
limit | Number | 一页多少条

```javascript 
  {
    "page": 1,
    "limit": 10
  }
```


### 响应


#### 成功

字段 | 类型  | 说明
:--- | :--- | :---
thumbnail | String | 247.5 * 116 缩略图
title | String | 工具名称
icon | String | 工具图标
description | String | 工具描述
id | String | 工具ID
url | String | 工具链接
pinyin | String | 工具拼音
publishedAt | String | 发布日期
publisher | String | 发布者
isTrending | Boolean | 是否热门
isApproved | Boolean | 是否审核通过
isAdmin | Boolean | 是否管理员发布

  ```json
  {
    "status": true,
    "message": "成功",
    "data": {
      list :  [
      {
        "thumbnail": "247.5*116",
        "title": "chatgpt",
        "icon": "xxx.png",
        "description": "chatgpt是一个开源的聊天机器人项目，基于GPT-3模型，可以实现自然语言对话和文本生成。",
        "id": 1,
        "url": "http://chatgpt.com",
        "pinyin": "chatgpt",
        "isTrending": true,
        "isApproved": true,
        "isAdmin": false,
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

#### 示例调用

使用 cURL 进行 API 调用的示例：

```bash
curl -X GET 'http://api.youyongba.com/pt' \
-H 'Content-Type: application/json' \
-d '{"page": 1, "limit": 10}'
```


