class Solution:
    def search(self, nums, target):
        """
        :type nums: List[int]
        :type target: int
        :rtype: int
        """
        if not nums:
            return -1
        
        left, right = 0, len(nums) - 1
        
        while left < right:
            mid = left + int((right - left) / 2)
            
            if target == nums[mid]:
                return mid
            
            elif nums[left] <= nums[mid]:
                # if left == mid, means left side is sorted. 
                # Eg:[3, 1] 
                # left = mid = 0, right = 1 left side is [3] right side is [3, 1]
                # 这里的左侧是指24行的比较所用的数字，右侧指30行的比较用到的数字。显然我们看到，左侧为[3],右侧为[3,1]
                if nums[left] <= target and target < nums[mid]:
                    right = mid - 1
                else:
                    left = mid + 1
                    
            else:
                if nums[mid] < target and target <= nums[right]:
                    left = mid + 1
                else:
                    right = mid - 1
                
                
        if nums[left] == target:
            return left
        else:
            return -1
        
        
        
