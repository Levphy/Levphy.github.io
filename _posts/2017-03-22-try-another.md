---
layout: post_layout
title: 发布 Kotlin 库到 Maven/JCenter仓库
time: 2016年04月12日 星期日
location: 上海
pulished: true
excerpt_separator: "```"
---
> 这篇文章主要主要用于测试我的博客版本
>
>```c++
>// 快速排序, 平均时间复杂度O(NlogN)
>void quickSort( int* A, int beg, int end )
>{
>    int i, j;
>    int pivot = A[beg];
>    if ( beg >= end ) return;   // 递归边界
>    i = beg;
>    j = end+1;
>    // 将数组分为小于pivot和大于pivot的两部分
>    for( ;; )
>    {
>        while( A[++i] < pivot );
>        while( A[--j] > pivot );
>        if ( i > j ) break;
>        swap( A[i], A[j] );
>    }
>    swap( A[beg], A[j] );
>    // 对两个子数组递归
>    quickSort( A, beg, j-1 );
>    quickSort( A, j+1, end );
>}
>```
