---
layout: default
title: LeetCode 算法
---

# LeetCode 算法题目（swift）

[TOC]

## 258.各位相加
题目：给定一个非负整数 num，反复将各个位上的数字相加，直到结果为一位数。
示例：
> 输入: 38
> 输出: 2 
> 解释: 各位相加的过程为：3 + 8 = 11, 1 + 1 = 2。 由于 2 是一位数，所以返回 2。

进阶:
你可以不使用循环或者递归，且在 O(1) 时间复杂度内解决这个问题吗？

```swift
class Solution {
    func addDigits(_ num: Int) -> Int {
        if  (num > 9){
            var kNum = num % 9
            if (kNum == 0) {
                return 9;
            }else {
                return kNum;
            }
        } else {
            return num
        }
    }
}
```


## 349.两个数组的交集

给定两个数组，编写一个函数来计算它们的交集。
示例 1：

> 输入: nums1 = [1,2,2,1], nums2 = [2,2]
> 输出: [2]

示例 2：

> 输入: nums1 = [4,9,5], nums2 = [9,4,9,8,4]
> 输出: [9,4]

说明：
输出结果中的每个元素一定是唯一的。
我们可以不考虑输出结果的顺序。

```swift
//  1. 转Set类型，直接交集。60 ms用时，8.00% 内存
class Solution {
    func intersection(_ nums1: [Int], _ nums2: [Int]) -> [Int] {
        let set1 = Set(nums1)
        let set2 = Set(nums2)
        let array = Array(set1.intersection(set2))
        return array
    }
}
```







[<< 返回首页](../)