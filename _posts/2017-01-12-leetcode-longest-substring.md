---
layout: post
author: Dong Yuan
title: [leetcode] Longest substring series, 3, 159, 340, 395
---

Summarizing the way of solving the longest substring problem in leetcode.

```
	3	Longest Substring Without Repeating Characters			23.7%	Medium	
	159	Longest Substring with At Most Two Distinct Characters			39.7%	Hard	
	340	Longest Substring with At Most K Distinct Characters		38.6%	Hard	
	395	Longest Substring with At Least K Repeating Characters			35.2%	Medium	
```

To solve this kind of problem, you should always think about two pointers with sliding window.

The template of codes should be:

```
	class Solution {
		int subString(string str, params...) {
			int i = 0, j = 0; //two pointers
			unordered_map<int> count;
			while(j < str.size()) {
				count[str[j]] ++;
				if(count[str[j]]...) {}
				//or
				while(count[str[j]]...) {}
				++j;
				//update the res
			}
			return *;
		}
	};
```

For [leetcode 3] we can also solve it with an map which record the last position of the charactors, update the map which traversing the string and the result.

For [Leetcode 395], we cannot solve it using this template, because ??? you should find the reason!!!


