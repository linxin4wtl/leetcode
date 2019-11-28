# https://leetcode.com/problems/two-sum/
# 答案
```
class Solution {
    public int[] twoSum(int[] nums, int target) {        
        int last = nums.length -1;
        
        HashMap<Integer, Integer> memo = new HashMap();
        
        for (int i = 0; i <= last; i++) {
            Integer complement = target - nums[i];
            
            if (memo.containsKey(complement)) {
                return new int[] {memo.get(complement), i};
            }
            
            memo.put(nums[i], i);
        }
        
        return null;
    }
}
```