The algorithm which is basically used to find the contiguous subarray (containing at least one number) which has the largest sum.


class Solution
{
    public int maxSubArray(int[] nums) 
    {
       if(nums.length  < 1)  return 0; 
        
        int currMax = nums[0], globalMax = nums[0];
        for(int i=1; i< nums.length; i++){
                currMax = Math.max(nums[i] + currMax , nums[i]);
                globalMax = Math.max(currMax, globalMax);
        }
        return globalMax;
    }
}



Given a array nums[] we are in the situation to find the maximum contiguous sum subarray. 

First we initialise two variables currMax and globalMax to first element of the array.

Then we loop through the array and check whether the  sum of currMax and the looped element is greater than the currMax.

If its greater then we assign the globalMax to currMax. 

Finally we return the globalMax.
