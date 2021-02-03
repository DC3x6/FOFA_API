# FOFA_API
README

功能：

- 支持多个语法查询
- 支持自定义返回字段
- 直接通过代理访问，无需使用VPN（需要保证连入公司网络且出口IP为 124.65.100.126 ）

配置：

所有配置均在info.ini文件中编辑。

【REQUESTS】

- email： 注册和登陆时时填写的email 

- key： 会员到个人资料可得到key，为32位的hash值 

- size：每页返回记录数，普通用户默认为10000条，vip用户默认为100条，最大可设置为10000条 

- page：翻页数，默认为第一页 

- full：默认为false，是否搜索全部数据，默认和页面搜索一样,只能搜索一年内的数据，指定为true搜索全部数据 

- fields：【自定义返回字段】

  字段列表，默认为host，用逗号分隔多个参数，如(fields=ip,title)，可选的列表有：host title ip domain port country province city country_name header server protocol banner cert isp as_number as_organization latitude longitude lastupdatetime

【KEYWORDS】

- q1 该参数为查询语法，可支持多个。

环境：

python3

pip install -r requirements.txt



运行：

编辑好配置文件后

python FOFA_API.py
