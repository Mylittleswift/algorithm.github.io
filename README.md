### Markdown

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```


| # | Title | Solution | Difficulty |
|---| ----- | -------- | ---------- |
|1|[Two Sum] | [Swift](./algorithms/swift/2Sum/2Sum.swift)|Easy|

## 1. Two Sum
_Easy_

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

Example:
```
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```
### Solution
```
class Solution {
    func twoSum(_ nums: [Int], _ target: Int) -> [Int] {
        var out: [Int] = []
       
        var dict:[Int: Int] = [:]     
        for (index,num) in nums.enumerated() {
            if let sum = dict[target - num] {
                out.append(index)
                out.append(sum)
            } 
            dict[num] = index
        }
        return out
    }
}
```
