group (组别) | 说明
---|---
pc | PC
ios | 苹果
android | 安卓
h5 | H5
wechat | 微信小程序
ali | 支付宝小程序
qq | QQ小程序
dingTalk | 钉钉小程序
touTiao | 头条小程序

> 注意：如果是商户 api 的需要安装商户插件，并创建用户信息进行登录

## 首页相关（不用access-token）


目录

- 读取塔罗师列表
- 通过用户名登录
- 通过手机号验证码快捷登录
- 重置令牌
- 注册
- 重置密码
- 退出登录

### 读取塔罗师列表
请求地址(Get)
```
/v2/common/tarot
```
参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
type | string| 否 | 无 | 类型 | all(默认：综合)|review(好评)|accurate(准确)|price(价格)

返回

```

{
    "code": 200,
    "message": "OK",
    "data": [
        {
            "id": "3",
            "merchant_id": "0",
            "category_id": "1",
            "title": "SS见",
            "description": "<p>SS见跳舞厉害</p>",
            "skill": "23323",
            "skill_image": "https://forest111.oss-cn-hangzhou.aliyuncs.com/tarot/pai/baojian10.jpg",
            "status": "1",
            "failed_reason": "",
            "position": "7",
            "ip": "183.130.11.124",
            "created_at": "1589029522",
            "updated_at": "1592489731",
            "tags": [
                {
                    "id": "2",
                    "merchant_id": "0",
                    "title": "事业",
                    "sort": "2",
                    "status": "1",
                    "created_at": "1592447257",
                    "updated_at": "1592484935"
                },
                {
                    "id": "4",
                    "merchant_id": "0",
                    "title": "财运",
                    "sort": "4",
                    "status": "1",
                    "created_at": "1592484893",
                    "updated_at": "1592484900"
                }
            ],
            "userinfo": {
                "id": "3",
                "nickname": "",
                "head_portrait": "",
                "gender": "0"
            }
        },
        {
            "id": "1",
            "merchant_id": "0",
            "category_id": "1",
            "title": "asdf",
            "description": "<p>asf</p>",
            "skill": "塔罗的`ASD",
            "skill_image": "asdfasdfasf",
            "status": "1",
            "failed_reason": "",
            "position": "1",
            "ip": "183.130.11.124",
            "created_at": "1588855905",
            "updated_at": "1592489842",
            "tags": [
                {
                    "id": "2",
                    "merchant_id": "0",
                    "title": "事业",
                    "sort": "2",
                    "status": "1",
                    "created_at": "1592447257",
                    "updated_at": "1592484935"
                }
            ],
            "userinfo": {
                "id": "1",
                "nickname": "hahaha",
                "head_portrait": "http://tl.6hmall.cn/attachment/images/2020/05/01/image_1588310505_J6E6b60u.jpg",
                "gender": "0"
            }
        }
    ],
    "timestamp": 1592614076
}



```

### 通过用户名登录

请求地址(Post)

```
/v2/common/account/login
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
username | string| 是 | 无 | 账号 |
password | string| 是 | 无 | 密码 | 
`group` | string| 是 | 无 | 组别 | 

返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "refresh_token": "1V1XLG8DQkROK6g-Rh5k17hZuZHQVZB9_1527339048",
        "access_token": "neRlaCJcbMQHgPmZqRjqYgVBfFZUe7lm_1527339048",
        "expiration_time": 172800,
        "member": {
            "id": 1,
            "username": "admin",
            "type": 1,
            "nickname": "简言",
            "realname": null,
            "head_portrait": null,
            "sex": 1,
            "qq": null,
            "email": "1@qq.com",
            "birthday": null,
            "user_money": "0.00",
            "accumulate_money": "0.00",
            "frozen_money": "0.00",
            "user_integral": 0,
            "address_id": "0",
            "visit_count": 8,
            "home_phone": null,
            "mobile": null,
            "role": 10,
            "last_time": 1527339048,
            "last_ip": "127.0.0.1",
            "provinces": 0,
            "city": 0,
            "area": 0,
            "allowance": 2,
            "allowance_updated_at": 1527339048,
            "status": 10,
            "append": 1511169880,
            "updated": 1527339048
        }
    }
}
```
### 通过手机号验证码快捷登录

请求地址(Post)

```
/v2/common/account/mobile-login
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
mibile | string| 是 | 无 | 手机号 |
code | string| 是 | 无 | 短信验证码 | 
`group` | string| 是 | 无 | 组别 | 

返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "refresh_token": "1V1XLG8DQkROK6g-Rh5k17hZuZHQVZB9_1527339048",
        "access_token": "neRlaCJcbMQHgPmZqRjqYgVBfFZUe7lm_1527339048",
        "expiration_time": 172800,
        "member": {
            "id": 1,
            "username": "admin",
            "type": 1,
            "nickname": "简言",
            "realname": null,
            "head_portrait": null,
            "sex": 1,
            "qq": null,
            "email": "1@qq.com",
            "birthday": null,
            "user_money": "0.00",
            "accumulate_money": "0.00",
            "frozen_money": "0.00",
            "user_integral": 0,
            "address_id": "0",
            "visit_count": 8,
            "home_phone": null,
            "mobile": null,
            "role": 10,
            "last_time": 1527339048,
            "last_ip": "127.0.0.1",
            "provinces": 0,
            "city": 0,
            "area": 0,
            "allowance": 2,
            "allowance_updated_at": 1527339048,
            "status": 10,
            "append": 1511169880,
            "updated": 1527339048
        }
    }
}
```
### 重置令牌

请求地址(Post)

```
/v2/common/account/refresh
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
refresh_token | string| 是 | 无 | 重置令牌 |
group | string| 是 | 无 | 组别 | 

返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "refresh_token": "ZQqIzE91lZsOsiBZUzX_HRvH_er71IA3_1527339061",
        "access_token": "y7ch3kQtRq7dEkqf6le2LOyRNOB_xzQV_1527339061",
        "expiration_time": 172800,
        "member": {
            "id": 1,
            "username": "admin",
            "type": 1,
            "nickname": "简言",
            "realname": null,
            "head_portrait": null,
            "sex": 1,
            "qq": null,
            "email": "1@qq.com",
            "birthday": null,
            "user_money": "0.00",
            "accumulate_money": "0.00",
            "frozen_money": "0.00",
            "user_integral": 0,
            "address_id": "0",
            "visit_count": 9,
            "home_phone": null,
            "mobile": null,
            "role": 10,
            "last_time": 1527339061,
            "last_ip": "127.0.0.1",
            "provinces": 0,
            "city": 0,
            "area": 0,
            "allowance": 2,
            "allowance_updated_at": 1527339061,
            "status": 10,
            "append": 1511169880,
            "updated": 1527339061
        }
    }
}
```
### 注册

请求地址(Post)

```
/v2/common/account/register
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
mobile | string| 是 | 无 | 手机 |
username | string| 是 | 无 | 用户名 |
realname | string| 否 | 无 | 真实姓名 |
code | string| 否 | 无 | 验证码目前不用 |
password | string| 是 | 无 | 密码 |
password_repetition | string| 是 | 无 | 再次输入密码 |
group | string| 是 | 无 | 组别 | 

返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "refresh_token": "WiFGpsyDShIn9NfvT1g7iPiUthk7R-2H_1588467118",
        "access_token": "9EwesesaVZdsdmgPdHnbJpZzsl5xV-TW_1588467118",
        "expiration_time": 7200,
        "member": {
            "mobile": "13888888888",
            "username": "xbb1",
            "realname": "我是小宝",
            "merchant_id": 0,
            "last_ip": "183.130.26.183",
            "last_time": 1588467118,
            "tree": "tr_0 ",
            "created_at": 1588467118,
            "updated_at": 1588467118,
            "id": 4,
            "visit_count": 1,
            "account": {
                "id": 4,
                "merchant_id": 0,
                "member_id": 4,
                "level": -1,
                "user_money": "0.00",
                "accumulate_money": "0.00",
                "give_money": "0.00",
                "consume_money": "0.00",
                "frozen_money": "0.00",
                "user_integral": 0,
                "accumulate_integral": 0,
                "give_integral": 0,
                "consume_integral": "0.00",
                "frozen_integral": 0,
                "status": 1
            }
        }
    },
    "timestamp": 1588467118
}
```
### 重置密码

请求地址(Post)

```
/v2/common/account/up-pwd
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
mobile | string| 是 | 无 | 手机 |
username | string| 是 | 无 | 用户名 |
code | string| 否 | 无 | 验证码目前不用 |
password | string| 是 | 无 | 密码 |
password_repetition | string| 是 | 无 | 再次输入密码 |
group | string| 是 | 无 | 组别 | 

返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "refresh_token": "WiFGpsyDShIn9NfvT1g7iPiUthk7R-2H_1588467118",
        "access_token": "9EwesesaVZdsdmgPdHnbJpZzsl5xV-TW_1588467118",
        "expiration_time": 7200,
        "member": {
            "mobile": "13888888888",
            "username": "xbb1",
            "realname": "我是小宝",
            "merchant_id": 0,
            "last_ip": "183.130.26.183",
            "last_time": 1588467118,
            "tree": "tr_0 ",
            "created_at": 1588467118,
            "updated_at": 1588467118,
            "id": 4,
            "visit_count": 1,
            "account": {
                "id": 4,
                "merchant_id": 0,
                "member_id": 4,
                "level": -1,
                "user_money": "0.00",
                "accumulate_money": "0.00",
                "give_money": "0.00",
                "consume_money": "0.00",
                "frozen_money": "0.00",
                "user_integral": 0,
                "accumulate_integral": 0,
                "give_integral": 0,
                "consume_integral": "0.00",
                "frozen_integral": 0,
                "status": 1
            }
        }
    },
    "timestamp": 1588467118
}

```
### 退出登录
请求地址(Post)

```
/v2/common/account/logout?access-token={access-token}
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---



返回

```
{
    "code": 200,
    "message": "退出成功",
    "data": [],
    "timestamp": 1588467798
}
```
