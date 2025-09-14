🚀 Day 05 – Python Sets

✅ What’s a Set?
An unordered, mutable collection of unique elements → {1, 2, 3, 'Py'}
Great for membership testing and removing duplicates.

⚡ Syntax Cheatsheet
# Create Set
s1 = {1, 2, 3}
s2 = set([1, 2, 2, 3])   # Duplicates removed → {1, 2, 3}
s3 = set()               # Empty set

# Add / Remove Elements
s1.add(4)
s1.remove(3)   # Raises KeyError if missing
s1.discard(5)  # No error if missing

# Set Operations
s1 = {1, 2, 3}
s2 = {3, 4, 5}

s1.union(s2)          # {1, 2, 3, 4, 5}
s1.intersection(s2)   # {3}
s1.difference(s2)     # {1, 2}
s1.symmetric_difference(s2)  # {1, 2, 4, 5}

# Membership Test
4 in s1   # True / False

✔️ Key Concepts
    • ✅ Unordered → No indexing (no s[0])
    • ✅ Unique Elements Only → duplicates auto-removed
    • ✅ Mutable → add() / remove()
    • ✅ Efficient membership → O(1) lookup time
    • ✅ Useful for set math → union, intersection, difference, symmetric difference

⚡ Problems to Master
1️⃣ Remove Duplicates from List
def remove_duplicates(lst): return list(set(lst))
2️⃣ Check Subset
def is_subset(small, big): return small <= big
3️⃣ Find Common Elements in Two Lists
def common_elements(l1, l2): return list(set(l1) & set(l2))

✅ DSA Essentials
    • Find Pair with Given Sum (Using Set)
def has_pair_with_sum(arr, target):
    seen = set()
    for num in arr:
        if target - num in seen:
            return True
        seen.add(num)
    return False
    • Find Unique Elements
def unique_elements(arr): return list(set(arr))
    • Check if List is Subset of Another
def is_subset(arr1, arr2): return set(arr1) <= set(arr2)

💡 Pro Tip
⚡ Sets are your best friend when needing fast membership tests & de-duplication.
👉 Avoid using lists when checking if element in collection in large data → sets are O(1).
