Problem link ( leet code ) : https://leetcode.com/problems/move-zeroes

( #1 Approach ) Java Code -> Two-Pass Approach or Shift-and-Fill Method 
```
class Solution {
    public void moveZeroes(int[] nums) {
        int zero_index = 0 ;
        for(int i=0;i<nums.length;i++)
        {
            if(nums[i]!=0)
            {
                nums[zero_index++]=nums[i];
            }
        }
        for(int i=zero_index;i<nums.length;i++)
        {
            nums[i]=0;
        }
    }
}
```


( #2 Approach ) Java Code -> Two Pointer Technique
```
class Solution {
    public void moveZeroes(int[] nums) {
        int zero_index = 0 ;
        for(int i=0;i<nums.length;i++)
        {
            if(nums[i]!=0)
            {
                if(i!=zero_index)
                {
                    int temp = nums[i];
                    nums[i] = nums[zero_index];
                    nums[zero_index] = temp;
                }
                zero_index++;
            }
        }
    }
}
```
