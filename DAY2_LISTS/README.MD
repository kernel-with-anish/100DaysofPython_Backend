🚀 Day 02 – Python Lists

✅ What’s a List?
An ordered, mutable collection of items → [1, 'Python', 3.14, True]

⚡ Syntax Cheatsheet
# Create List
lst = [1, 2, 3, 'Py']

# Access Elements
lst[0], lst[-1], lst[1:3], lst[::-1]

# Add Elements
lst.append(4)
lst.insert(1, 'InsertHere')

# Remove Elements
lst.pop()          # Removes last
lst.remove('Py')   # Removes first occurrence

# Useful Methods
len(lst), lst.index(2), lst.count(1), lst.sort(), lst.reverse()

✔️ Key Concepts
    • Mutable → can change elements.
    • Mixed Data Types Allowed → [1, 'a', True, 3.14]
    • Slicing Works → lst[1:4], lst[::-1]
    • Nested Lists → lst = [[1,2], [3,4]] → Access: lst[1][0]

⚡ Problems to Master
1️⃣ Sum of List Elements
def list_sum(lst): return sum(lst)
2️⃣ Find Maximum in List
def find_max(lst): return max(lst)
3️⃣ Flatten a Nested List
def flatten(lst): return [item for sub in lst for item in sub]

✅ DSA Essentials
    • Two Sum Problem (Hash Map)
def two_sum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        if target - num in seen:
            return [seen[target - num], i]
        seen[num] = i
    • Move Zeroes to End
def move_zeroes(nums):
    i = 0
    for num in nums:
        if num != 0:
            nums[i] = num
            i += 1
    while i < len(nums):
        nums[i] = 0
        i += 1
    • Find Duplicate in List
def find_duplicate(nums):
    seen = set()
    for num in nums:
        if num in seen: return num
        seen.add(num)
    return -1

💡 Pro Tip
⚡ Always prefer append() over + [element] inside loops → faster and avoids new list creation.
👉 For performance & clean code.
