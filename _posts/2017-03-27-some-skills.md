---
layout: post_layout
title: 一些二进制位判断技巧
time: 2017年03月27日 星期一
location: 武汉
pulished: true
excerpt_separator: "```"
---
总结下目前已知的二进制数的一些特征判断技巧:

​	1.判断一个数是不是2^n

> ```c
> bool fun(int i){
>     return (i > 0) && ((i & (i - 1)) == 0);
> }
> ```

原理是假如x为2的N次方整数，由于2的N次方的数二进制表示是第1位(最高位)为1，其余为0，而x-1得到的数的二进制表示恰恰是第1位为0，其余为1，两者按位与，结果为0，否则假设不成立。

​	2.统计一个数，其二进制形式中0的个数

```c
int fun(unsigned int x)
{
    int n = 0;
    while(x+1)
    {
        n++;
        x = x | (x+1);
    }
    return n;
}
```

其原理是，每次循环当中，把x的二进制从右往左的最后一位0变成1，当x全为1时，x+1溢出为0，结束循环，返回统计结果。

​	3.统计一个数，其二进制形式中1的个数

```c
int fun(unsigned int x)
{
    int n = 0;
    while(x)
    {
        n++;
        x = x & (x-1);
    }
    return n;
}
```

其原理与2类似，每次循环当中，把x的二进制从右往左的最后一位1变成0，当x全为0时，结束循环，返回统计结果。注意循环条件和位运算表达式与2中的区别



如果其他技巧，未来再进行补充  -_-