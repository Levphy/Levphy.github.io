---
layout: post_layout
title: 博客测试
time: 2017年03月22日 星期三
location: 武汉
pulished: true
excerpt_separator: "```"
---
> 这篇文章主要主要用于测试我新搭建的博客，但是目前还不太习惯于markdown写博客，学习中 -_-
>
> ```c++
> // 快速排序, 平均时间复杂度O(NlogN)
> void quickSort( int* A, int beg, int end )
> {
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
> }
> ```
