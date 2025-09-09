// https://leetcode.com/problems/squares-of-a-sorted-array/

// Normal Approach

class Solution {
    public int[] sortedSquares(int[] nums) {
        for(int i =0;i<nums.length;i++) {
            nums[i] = Math.abs(nums[i]*nums[i]);
        }
        Arrays.sort(nums);
        return nums;
    }
}

// Two pointer Approach
class Solution {
    public int[] sortedSquares(int[] nums) {
        int l = 0, r = nums.length-1;
        int ans[] = new int[nums.length];
        while(l<=r) {
            ans[l] = nums[l] * nums[l];
            ans[r] = nums[r] * nums[r];
            l++;
            r--;
        }
        Arrays.sort(ans);
        return ans;
    }
}
