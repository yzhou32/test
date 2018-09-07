# 一\. Api文档—cloud所有在线文档
apply-controller
---
## 1\. 创建ec2申请
#### 接口功能
通过传入ApplyEc2对象创建ec2申请，返回flowid

#### URI
/api/ec2apply/create

#### HTTP请求方式
POST

#### 请求参数
|  参数 | 描述 | 参数类型 | 数据类型 |
| --- | --- | --- | --- |
| applyId | 申请id,创建申请时不用暴露出了 | query | string |
| region | 区域,获取后用户选择 | query | string |
| imageId | 镜像,获取后用户选择 | query | string |
| insType | 类型,获取后用户选择 | query | string |
| ec2Count | 数量,用户自己填写 | query | integer |
| keyName | 密钥对,获取后用户选择,也可以选择创建 | query | string |
| sg | 安全组,获取后用户选择 | query | string |
| vpc | vpc,获取后用户选择 | query | string |
| subnet | 子网，获取后用户选择 | query | string |
| usePubip | 公共ip | query | boolean |
| useFlexip | 弹性ip | query | boolean |
| volumeSize | ebs大小 | query | integer |
| volumeType | ebs类型 | query | string |
| desc | 描述 | query | string |
| status | 状态 | query | integer |
| frontApp | 接收前端传来的数据 | body | ApplyEc2 |


#### 响应消息
|HTTP 状态码|语义|备注|
|:-----   |:------|:-----------------------------   |
|201   | Created | |
|401  | Unauthorized | |
|403 | Forbidden | |
|404 | Not Found | |
