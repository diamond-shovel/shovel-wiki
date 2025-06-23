# 资产是什么

在此项目中，资产代指**数字资产**，约定的基本属性有:


|属性|描述|
|---|---|
|name|资产的名称|
|properties|资产的属性列表|
|responsible_entity|资产的负责实体|

properties的属性列表为`Dict[str, Any]`类型，可以包含任意键值对。

项目中所展示的资产为`WebAsset`，参考[httpx](https://github.com/projectdiscovery/httpx)项目的Web资产定义，集成了基本属性，定义如下

|属性|类型|解释
|---|---|---|
finger_print_id|int|资产指纹ID，通过int(hashlib.md5(f"{host}{url}{str(status_code)}".encode()).hexdigest(), 16)计算 
group_id|int|资产组ID
host|str|host
url|str|URL
title|Optional[str]|标题
scheme|Optional[str]|协议（如http, https）
webserver|Optional[str]|Web服务器信息
content_type|Optional[str]|内容类型
method|Optional[str]|HTTP方法（如GET, POST）
path|Optional[str]|路径
time|Optional[datetime]|发现时间戳
a|Optional[str]|A记录
tech|Optional[str]|技术栈
words|Optional[int]|字数
lines|Optional[int]|行数
status_code|Optional[int]|HTTP状态码
content_length|Optional[int]|内容长度
failed|Optional[str]|失败信息
final_url|Optional[str]|最终URL
chain_status_codes|Optional[str]|状态码链
cname|Optional[str]|CNAME记录
jarm_hash|Optional[str]|JARM哈希
favicon|Optional[str]|favicon图标
favicon_url|Optional[str]|favicon URL
favicon_path|Optional[str]|favicon路径
location|Optional[str]|位置
aaaa|Optional[str]|AAAA记录
responsible_entity|str|资产的负责实体
