---
layout: post
title: "python time"
description: ""
category: tech
tags: [tech]
---
{% include JB/setup %}

在python中获得当前时间，总是写的时候再去查，效率太低，写在blog里，备用

取得当前时间的时间戳 (时间戳好像是1970年到现在时间相隔的时间)：
import time
print time.time()
输出的结果是：
1362127742.093816

time.localtime(time.time())
用time.localtime()方法，作用是格式化时间戳为本地的时间。
>>> time.localtime(time.time())
time.struct_time(tm_year=2013, tm_mon=3, tm_mday=1, tm_hour=16, tm_min=50, tm_sec=50, tm_wday=4, tm_yday=60, tm_isdst=0)

>>> time.strftime('%Y-%m-%d',time.localtime(time.time()))
'2013-03-01'


time.strftime里面有很多参数，可以让你能够更随意的输出自己想要的东西：
下面是time.strftime的参数：
strftime(format[, tuple]) -> string
将指定的struct_time(默认为当前时间)，根据指定的格式化字符串输出
python中时间日期格式化符号：
%y 两位数的年份表示（00-99）
%Y 四位数的年份表示（000-9999）
%m 月份（01-12）
%d 月内中的一天（0-31）
%H 24小时制小时数（0-23）
%I 12小时制小时数（01-12）
%M 分钟数（00=59）
%S 秒（00-59）

%a 本地简化星期名称
%A 本地完整星期名称
%b 本地简化的月份名称
%B 本地完整的月份名称
%c 本地相应的日期表示和时间表示
%j 年内的一天（001-366）
%p 本地A.M.或P.M.的等价符
%U 一年中的星期数（00-53）星期天为星期的开始
%w 星期（0-6），星期天为星期的开始
%W 一年中的星期数（00-53）星期一为星期的开始
%x 本地相应的日期表示
%X 本地相应的时间表示
%Z 当前时区的名称
%% %号本身

