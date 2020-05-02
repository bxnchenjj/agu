提问列表
GET：`http://tl.6hmall.cn/api/v1/ask/questions`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| page      | string   |   要读取的分页码     |页码 |

提问
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
查看提问详情
GET：`http://tl.6hmall.cn/api/v1/ask/questions/2`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| id      | string   |   id     |直接带在URL上|
| page       | string   |   要读取的分页码     |直接带在URL上|

回答问题
POST：`http://tl.6hmall.cn/api/v1/ask/answers/store`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| question_id      | string   |   问题ID    ||
| content       | string   |   回复的内容     |必填|

修改头像和昵称
POST：`http://tl.6hmall.cn/api/v1/site/up-userinfo`
入参说明

| 参数名        | 类型   |  说明  |备注|
| --------   | -----:  | :----:  |:----: |
| nickname       | string   |   昵称    ||
| head_portrait        | string   |   头像     |可不填|
| realname           | string   |   真实姓名     | 可不填|





