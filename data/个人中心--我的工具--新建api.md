## 个人中心 -- 我的工具 -- 新建API
### 创建新的自研工具

> POST

- https://api.youyong.ba/my-tools/create

### header

```javascript
{
    "Authorization": "Bearer xxx",
    "Content-Type": "application/json"
}
```

### 参数

| 参数名       | 类型   | 描述               |
| ------------ | ------ | ------------------ |
| title        | String | 工具标题           |
| description  | String | 工具描述           |
| icon         | String | 工具图标链接       |
| url          | String | 工具链接           |
| pinyin       | String | 工具名称拼音       |
|     thumbnail   | String | 缩略图       |
|      categoryType  | String |     用户工具类别   |




```json
{
  "title": "创新编程辅助工具N",
  "description": "结合最新技术研发的编程辅助工具，旨在提高开发效率，简化复杂编程任务，支持多种编程语言，适合初学者和资深开发者。",
  "icon": "http://example.com/icon14.png",
  "url": "http://example.com/toolN",
  "pinyin": "chuangxinbianchengfuzhugongju",
}
```

### 响应

#### 成功

```json
{
  "status": true,
  "message": "工具创建成功",
  "data": {
    "id": 14,
    "title": "创新编程辅助工具N",
    "description": "结合最新技术研发的编程辅助工具，旨在提高开发效率，简化复杂编程任务，支持多种编程语言，适合初学者和资深开发者。",
    "icon": "http://example.com/icon14.png",
    "url": "http://example.com/toolN",
    "pinyin": "chuangxinbianchengfuzhugongju",
    "isTrending": false,
    "publishedAt": "2024-01-07",
    "publisher": "用户ID"
  }
}
```

#### 失败

```json
{
  "status": false,
  "message": "创建工具失败，[具体原因]"
}
```

### 示例调用

```bash
curl -X POST 'https://api.youyong.ba/my-tools/create' \
-H 'Authorization: Bearer xxx' \
-H 'Content-Type: application/json' \
-d '{
      "title": "创新编程辅助工具N",
      "description": "结合最新技术研发的编程辅助工具，旨在提高开发效率，简化复杂编程任务，支持多种编程语言，适合初学者和资深开发者。",
      "icon": "http://example.com/icon14.png",
      "url": "http://example.com/toolN",
      "pinyin": "chuangxinbianchengfuzhugongju",
      "isTrending": false
    }'
```