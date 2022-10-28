[Click here to view question](https://leetcode.com/problems/maximum-subarray/)
<br/>
Given an integer array nums, find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.
<br/>
A **subarray** is a **contiguous** part of an array.

**Example 1:**

Input: nums = [-2,1,-3,4,-1,2,1,-5,4]<br/>
Output: 6<br/>
Explanation: [4,-1,2,1] has the largest sum = 6.<br/>


**Example 2:**

Input: nums = [1]<br/>
Output: 1

**Example 3:**

Input: nums = [5,4,-1,7,8]<br/>
Output: 23


##Solution
(`
class Solution {
    public int maxSubArray(int[] nums) {
        int n = nums.length; //length of array
        int max = Integer.MIN_VALUE, sum = 0;//initial condition
        
        for(int i=0;i<n;i++){
            // addiding each element
            sum = sum + nums[i];
            // finding max element
            max = Math.max(sum,max);
            // condition
            if(sum<0){
                sum = 0;
            }
        }
        
        return max;
    }
}
)