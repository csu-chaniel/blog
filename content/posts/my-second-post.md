+++
title = 'My Second Post'
date = 2024-09-26T20:37:58+08:00
draft = true
+++
![这是图片](https://img0.baidu.com/it/u=3946773676,476453382&fm=253&fmt=auto&app=120&f=JPEG?w=640&h=401")

给你单链表的头指针 head 和两个整数 left 和 right
## Introduction
second

This is **bold** text, and this is *emphasized* text.

Visit the [Hugo](https://gohugo.io) website!

以上
 ，其中 left <= right 。请你反转从位置 left 到位置 right 的链表节点，返回 反转后的链表 。

给你单链表的头指针 head 和两个整数 left 和 right ，其中 left <= right 。请你反转从位置 left 到位置 right 的链表节点，返回 反转后的链表 。

给你单链表的头指针 head 和两个整数 left 和 right ，其中 left <= right 。请你反转从位置 left 到位置 right 的链表节点，返回 反转后的链表 。

```go
func pivotIndex(nums []int) int {
	n := len(nums)
	prefix := make([]int, n)
	suffix := make([]int, n)
	for i := 1; i < n; i++ {
		prefix[i] = prefix[i-1] + nums[i-1]
		suffix[n-i-1] = suffix[n-i] + nums[n-i]
	}
	for i := 0; i < n; i++ {
		if prefix[i] == suffix[i] {
			return i
		}
	}
	return -1
}
```