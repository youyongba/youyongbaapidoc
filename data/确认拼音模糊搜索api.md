# 拼音模糊搜索 API

## 获取匹配拼音的工具列表

> get

- https://api.youyongba.com/pysearch

### header

```javascript
{
    "Authorization": "Bearer xxx"
}
```

### 参数
> `application/json`

用于根据工具的拼音进行模糊搜索。无需在 URL 中传递参数。默认是 `page=1`, `limit=10`。

| 字段   | 类型   | 说明                       |
| :----- | :----- | :------------------------- |
| page   | Number | 第几页                     |
| limit  | Number | 一页多少条                 |
| pinyin | String | 工具的拼音（支持模糊匹配） |

```javascript 
  {
    "page": 1,
    "limit": 10,
    "pinyin": "chatgpt"
  }
```

### 响应

#### 成功

| 字段        | 类型    | 说明                     |
| :---------- | :------ | :----------------------- |
| thumbnail   | String  | 缩略图尺寸为 247.5 * 116 |
| title       | String  | 工具名称                 |
| icon        | String  | 工具图标                 |
| description | String  | 工具描述                 |
| id          | String  | 工具ID                   |
| url         | String  | 工具链接                 |
| pinyin      | String  | 工具拼音                 |
| publishedAt | String  | 发布日期                 |
| publisher   | String  | 发布者                   |
| isTrending  | Boolean | 是否热门                 |
| isApproved  | Boolean | 是否审核通过             |
| isAdmin     | Boolean | 是否管理员发布           |

```json
{
  "status": true,
  "message": "成功",
  "data": {
    "list": [{
      "thumbnail": "247.5*116",
      "title": "示例工具",
      "icon": "example.png",
      "description": "这是一个示例工具，用于演示拼音模糊搜索API的响应结构。",
      "id": "exampleID",
      "url": "http://example.com",
      "pinyin": "shili",
      "isTrending": false,
      "isApproved": true,
      "isAdmin": false,
      "publishedAt": "2022-02-02",
      "publisher": "李四"
    }
    // 可能包含更多匹配项...
  ],
  "total": 1123,
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
curl -X GET 'http://api.youyongba.com/pysearch' \
-H 'Content-Type: application/json' \
-d '{"page": 1, "limit": 10, "pinyin": "shili"}'
```