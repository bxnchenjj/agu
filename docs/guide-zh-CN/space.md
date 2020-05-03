## 个人中心

目录

- 认证查看
- 提交认证
- 我的提问
- 我的回答
- 邀我回答
- 我的通知
- 我的消息

> 

#### 认证查看

（Get）:

```
/api/profile/authentication
```

返回

```
{
    "code": 200,
    "message": "创建成功",
    "data": {
        "id": 1,
        "merchant_id": 0,
        "category_id": 1,
        "title": "asdf",
        "description": "asf",
        "skill": "塔罗的",
        "skill_image": "http://tl.6hmall.cn/attachment/images/2020/05/01/image_1588310505_J6E6b60u.jpg",
        "status": 2,
        "failed_reason": "111",
        "position": 7,
        "ip": "183.130.26.183",
        "created_at": 1588399140,
        "updated_at": 1588491244
    },
    "timestamp": 1588491456
}

```

#### 提交认证

（Post）:

```
/api/profile/authentication/store
```

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
title | string | 是 | 无 |  身份职业| 
description | string | 是 | 无 | 自我介绍
skill | string | 是 | 无 | 认证领域 | 
skill_img | string | 是 | 无 | 专业性证明 | 认证的图片URL，需先上传

返回

```
{
    "code": 200,
    "message": "OK",
    "data": [
    ],
    "timestamp": 1588409635
}


```
