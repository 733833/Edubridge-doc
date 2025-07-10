Given an array of integers and a target sum, return indices of the two numbers that add up to the target
def two_sum(nums, target):
    num_map = {}
    for i, num in enumerate(nums):
        diff = target - num
        if diff in num_map:
            return [num_map[diff], i]
        num_map[num] = i
    return []
