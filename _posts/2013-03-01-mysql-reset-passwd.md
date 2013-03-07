---
layout: post
title: "mysql reset passwd"
description: ""
category: tech
tags: [tech]
---
{% include JB/setup %}

今天尝试用Acunetix Web Vulnerability Scanner扫描网站漏洞，运行时间特别长，没有扫描出有效的漏洞，但是导致了我的mysql连接不上。
具体是什么原因导致mysql连接不了还木有找到，但是重置了数据库密码后就又可以连接了，重置的方法：
二、方法
首先停止mysql服务：
sc stop mysql
然后：
mysqld --skip-grant-tables
另开一个终端，继续
mysqlcheck --check-upgrade --all-databases --auto-repair
然后再输入
mysql

use mysql
 update user set password='' where user='root';
 flush privileges;

mysqlcheck --check-upgrade --all-databases --auto-repair
