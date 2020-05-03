目录

- 提问列表(公用)
- 发起提问
- 查看提问详情
- 回答问题


### 1、提问列表(公用)

GET：`http://tl.6hmall.cn/api/v1/ask/questions`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| page      | string   |   要读取的分页码     |页码 |

返回

```
{
    "code": 200,
    "message": "OK",
    "data": [
        {
            "id": "22",
            "merchant_id": "0",
            "member_id": "3",
            "category_id": "1",
            "title": "这个标题厉害了",
            "description": "网络送礼分类扫雷扫雷扫雷扫雷受伤了拉夫劳伦了了了了流量 看看看看看发发发洒飞是是是是是是是是",
            "img": "http://tl.6hmall.cn/attachment/images/2020/05/01/image_1588314011_YcC2TeUv.png",
            "price": "0",
            "hide": "0",
            "answers": "0",
            "views": "0",
            "followers": "0",
            "collections": "0",
            "comments": "0",
            "status": "0",
            "ip": "61.164.96.42",
            "created_at": "1588314011",
            "updated_at": "1588314011"
        },
    ],
    "timestamp": 1588409635
}


```


2、发起提问
POST：`http://tl.6hmall.cn/api/v1/ask/questions/create`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| category_id      | string   |   分类ID     ||
| title       | string   |   标题     ||
| description	      | string   |   描述    ||
| answer_id		      | string   |   回答者ID     ||
| img		      | string   |   图片URL     ||
| price				      | string   |   悬赏分数金额     |  |
返回

```

{
    "code": 200,
    "message": "创建成功",
    "data": [],
    "timestamp": 1588409587
}
```

3、查看提问详情
GET：`http://tl.6hmall.cn/api/v1/ask/questions/2`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| id      | string   |   id     |直接带在URL上|
| page       | string   |   要读取的分页码     |直接带在URL上|

返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "question": {
            "id": 1,
            "merchant_id": 0,
            "member_id": 1,
            "category_id": 1,
            "title": "天天喝酒",
            "description": "天天喝酒的描述",
            "img": "http://tl.6hmall.cn/attachment/images/2020/04/25/image_1587806389_QwTStjlc.jpg",
            "price": 10,
            "hide": 0,
            "answers": 0,
            "views": 0,
            "followers": 0,
            "collections": 0,
            "comments": 0,
            "status": 0,
            "ip": "115.219.135.131",
            "created_at": null,
            "updated_at": null
        },
        "answers": [
            {
                "id": "1",
                "merchant_id": "0",
                "question_title": "我喜欢读书",
                "question_id": "1",
                "member_id": "2",
                "content": "<p><span style=\"color:rgb(51,51,51);\">好好的看书吧，小伙</span><span style=\"color:rgb(51,51,51);\">好好的看书吧，小伙</span><span style=\"color:rgb(51,51,51);\">好好的看书吧，小伙</span><span style=\"color:rgb(51,51,51);\">好好的看书吧，小伙</span><span style=\"color:rgb(51,51,51);\">好好的看书吧，小伙</span><br></p>",
                "supports": "0",
                "oppositions": "0",
                "comments": "0",
                "status": "1",
                "adopted_at": null,
                "created_at": "1588255643",
                "updated_at": "1588255643",
                "member": {
                    "id": "2",
                    "nickname": "",
                    "head_portrait": "",
                    "gender": "0"
                }
            }
        ]
    },
    "timestamp": 1588409267
}
```

4、回答问题（如果指定谁回答，那么别人是回答不了的）
POST：`http://tl.6hmall.cn/api/v1/ask/answers/store`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| question_id      | string   |   问题ID    ||
| content       | string   |   回复的内容     |必填|
返回

```
{
    "code": 200,
    "message": "创建成功",
    "data": [],
    "timestamp": 1588409381
}


```

