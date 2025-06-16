# june16_2025
The problems that I solved today

Given a 0-indexed integer array nums of size n, find the maximum difference between nums[i] and nums[j] (i.e., nums[j] - nums[i]), such that 0 <= i < j < n and nums[i] < nums[j].

Return the maximum difference. If no such i and j exists, return -1.

Code:
class Solution {
    public int maximumDifference(int[] nums) {
        int ans=-1;
        int n=nums.length;
        for(int i=0;i<n;i++)
        {
            for(int j=i+1;j<n;j++)
            {
                if(nums[i]<nums[j])   
                    ans=Math.max(ans,nums[j]-nums[i]);
            }
        }
        return ans;
    }
}
