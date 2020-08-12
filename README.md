# LeetCode-
按数据结构与算法归纳整理在LeetCode刷的题

class Solution {
    public int maxSubArray(int[] nums) {
        if(nums.length == 0)
            return -2147483648;
        int max=nums[0];
        int sum=nums[0];
        for(int i=1;i<nums.length;i++){
            sum=sum+nums[i]>nums[i]?sum+nums[i]:nums[i];
            max=max>sum?max:sum;
        }
        return max;
    }
}
