# JAVA_slidingWindow

maximum_consecutive_ones_III
--------------------------------------------------------------------------------------------------------------------------------------------------------------


class Solution {
public int longestOnes(int[] nums, int k) {
       
        int zeroCount=0;
        int left=0;
        int i=0;
        int n=nums.length-1;
        int maxLen=0;
        
        while(i<=n){
            if(nums[i]==0){
                zeroCount++;
            }
            while(zeroCount>k){
               if(nums[left]==0){
                 zeroCount--;
               }
                left++;   
            }
            if(zeroCount<=k){
                maxLen=Math.max(maxLen,i-left+1);
            }
            i++;
        }
        return maxLen;
    }
}

----------------------------------------------------------------------------------------------------------------------------------------------------------------
