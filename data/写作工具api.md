## 写作工具
### 获取写作工具列表

> GET

- https://api.example.com/writing-tools

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

### 响应

#### 成功

| 参数名        | 类型   | 描述           |
| ----------- | ------ | -------------- |
| thumbnail   | String | 缩略图         |
| title       | String | 标题           |
| icon        | String | 图标           |
| description | String | 描述           |
| id          | Number | ID             |
| url         | String | 工具链接       |
| pinyin      | String | 拼音           |
| publishedAt | String | 发布日期       |
| publisher   | String | 发布者         |

### 示例调用

使用 cURL 进行API调用的示例：

```bash
curl -X GET 'https://api.youyong.ba/writing-tools?page=1&limit=10'
```

