---
title: "[leetcode] Two Sum"
categories:
  - leetcode
tags:
  - [leetcode, blog]
toc: true
toc_sticky: true
toc_label: "목차"
---

##Python
~~~python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i in range(0, len(nums)):
            for j in range(i + 1, len(nums)):
                if nums[i] + nums[j] == target:
                    return [i, j]
~~~