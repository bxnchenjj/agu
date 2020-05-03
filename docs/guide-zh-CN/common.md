### 获取省市区

请求地址(Get)

```
/v1/common/provinces?access-token={access-token}&pid=110000
```

参数

参数名 | 参数类型 | 必填 | 默认 | 说明 | 备注
---|---|---|---|---|---
pid | string| 否 | 无 | 没有的时候取全国省份有的时候取对应的下级 |

返回

```
{
    "code": 200,
    "message": "OK",
    "data": [
        {
            "id": "110100",
            "title": "市辖区",
            "pid": "110000"
        }
    ],
    "timestamp": 1588469015
}
```
