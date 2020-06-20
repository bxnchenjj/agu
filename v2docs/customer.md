
[个人中心](v2docs/profile.md)


## 


目录
- 重置令牌
- 修改个人资料
- 退出登录

### 重置令牌

请求地址(Post)

```
/v2/customer/account/refresh
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
### 修改个人资料

请求地址(Post)

```
/v2/customer/account/up-userinfo
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
nickname | string| 是 | 无 | 昵称 |
head_portrait | string| 否 | 无 | 头像URL | 
realname | string| 否 | 无 | 真实姓名 | 
返回

```
{
    "code": 200,
    "message": "OK",
    "data": {
        "refresh_token": "ZQqIzE91lZsOsiBZUzX_HRvH_er71IA3_1527339061",
        "access_token": "y7ch3kQtRq7dEkqf6le2LOyRNOB_xzQV_1527339061",
        "expiration_time": 7200,
        "member": {
            "id": 1,
            "merchant_id": 0,
            "username": "test",
            "type": 1,
            "nickname": "简言",
            "realname": null,
            "head_portrait": null,
            "current_level": 1,
            "gender": 0,
            "qq": "",
            "email": "",
            "birthday": null,
            "visit_count": 37,
            "home_phone": "",
            "mobile": "",
            "role": 10,
            "last_time": 1588466624,
            "last_ip": "183.130.26.183",
            "province_id": 0,
            "city_id": 0,
            "area_id": 0,
            "pid": 0,
            "level": 1,
            "tree": "tr_0 ",
            "promo_code": "",
            "status": 1,
            "created_at": 1587800350,
            "updated_at": 1588466624,
            "status": 1,
            "append": 1511169880,
            "updated": 1527339061,
            "account": {
                "id": 1,
                "merchant_id": 0,
                "member_id": 1,
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
    }
}
```
### 退出登录
请求地址(Post)

```
/v2/customer/account/logout?access-token={access-token}
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

