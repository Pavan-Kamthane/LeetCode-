[view question](https://leetcode.com/problems/running-sum-of-1d-array/) <br/>

Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).<br/>

Return the running sum of nums.<br/>

 

Example 1: <br/>

Input: nums = [1,2,3,4]<br/>
Output: [1,3,6,10]<br/>
Explanation: Running sum is obtained as follows: [1, 1+2, 1+2+3, 1+2+3+4].<br/>

Example 2:<br/>

Input: nums = [1,1,1,1,1]<br/>
Output: [1,2,3,4,5]<br/>
Explanation: Running sum is obtained as follows: [1, 1+1, 1+1+1, 1+1+1+1, 1+1+1+1+1].<br/>

Example 3:<br/>

Input: nums = [3,1,2,10,1]<br/>
Output: [3,4,6,16,17]<br/>

```
class Solution {
    public int[] runningSum(int[] nums) {
         for(int i=1;i<nums.length;i++){
        nums[i]= nums[i]+nums[i-1];
    }
    return nums;
    }
}
```