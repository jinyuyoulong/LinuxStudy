nslookup作用

nslookup用于查询DNS的记录，查询域名解析是否正常，在网络故障时用来诊断网络问题
--------------------------------------------------------------------------------
查询

a. 直接查询

nslookup domain [dns-server]

  //如果没有指定dns服务器，就采用系统默认的dns服务器。

b. 查询其他记录

nslookup -qt = type domain [dns-server]
```
type:
    A -->地址记录
    AAAA   -->地址记录
    AFSDB Andrew    -->文件系统数据库服务器记录
    ATMA -->ATM地址记录
    CNAME   -->别名记录
    HINHO  -->硬件配置记录，包括CPU、操作系统信息 
    ISDN   -->域名对应的ISDN号码
    MB   -->存放指定邮箱的服务器
    MG    -->邮件组记录
    MINFO   -->邮件组和邮箱的信息记录
    MR   -->改名的邮箱记录
    MX   -->邮件服务器记录
    NS  --> 名字服务器记录
    PTR    ->反向记录
    RP    -->负责人记录
    RT  -->路由穿透记录
    SRV    -->TCP服务器信息记录
    TXT   -->域名对应的文本信息
    X25  -->域名对应的X.25地址记录
```
c. 查询更具体的信息

nslookup -d [其他参数] domain [dns-server]    

//只要在查询的时候，加上-d参数，即可查询域名的缓存
