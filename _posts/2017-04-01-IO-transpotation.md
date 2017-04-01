---
layout: post_layout
title: C/C++常见字符串与数字之间的转换
time: 2017年04月01日 星期六
location: 武汉
pulished: true
excerpt_separator: "```"
---
常见的字符串与数字之间的转换

1. 平台有关

   itoa()、atoi()、atol()、atof()等函数，属于C语言函数，但需要注意的是，这些函数不属于标准C内容，跟平台相关，通用性、可移植性较差，无法使用很正常。

2. 平台无关

   数字---->字符串   C语言: sprintf()函数    C++: ostringstream    C++11: to_string()函数

   字符串---->数字   C语言: sscanf()函数    C++: istringstream      C++11: stoi()、stol()、stoll()[字符串转long long类型]、stoull()[转unsigned long long]、stof()[转float]、stod()[转double]、stold()[转long double]

3. 示例