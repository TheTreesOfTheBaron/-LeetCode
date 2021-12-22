## Problem
https://leetcode-cn.com/problems/que-shi-de-shu-zi-lcof/

## Solution
1. nums[index] should == index
2. edge case: [0,1,2], missing 3; [1], missing 0; [0], missing 1
3. Can loop through the array but O(n), not the best
4. Binary search


## Code
```java
class Solution {
    public int missingNumber(int[] nums) {
        int left = 0, right = nums.length-1, middle ;

        while(left < right){
            middle = (left + right)/2;
            if(nums[middle] == middle){ //the num isn't on the left side
                left = middle + 1;
            }else{ // on the right side
                right = middle;
            }
        }
        return nums[right] == right ? right + 1 : right;

    }
}


```

## Complexity
Time: O(logN)

Space: O(1)

## Thoughts
1. 排序数组中的搜索问题，首先想到 二分法 binary search 解决