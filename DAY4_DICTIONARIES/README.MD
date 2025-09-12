🚀 Day 04 – Python Dictionaries

✅ What’s a Dictionary?
An unordered, mutable collection of key-value pairs → {key: value}
Example → {'name': 'Anish', 'age': 19, 'tech': 'Python'}

⚡ Syntax Cheatsheet
# Create Dict
d1 = {'name': 'Anish', 'age': 19}
d2 = dict(name='Anish', age=19)
d3 = {}  # Empty dict

# Access Values
d1['name']       # 'Anish'
d1.get('age')    # 19

# Add / Update
d1['language'] = 'Python'
d1['age'] = 20

# Delete
del d1['age']
d1.pop('language')

# Keys & Values
d1.keys(), d1.values(), d1.items()

# Iteration
for key, value in d1.items():
    print(f"{key}: {value}")

✔️ Key Concepts
    • Mutable → Can add/update/delete key-value pairs
    • Keys must be hashable (tuples, strings, numbers); values can be any type
    • Useful for fast O(1) lookups
    • Nested Dict →
d = {'person': {'name': 'Anish', 'age': 19}}
d['person']['name']  # 'Anish'

⚡ Problems to Master
1️⃣ Merge Two Dictionaries
def merge_dicts(d1, d2): return {**d1, **d2}
2️⃣ Count Character Frequency in String
from collections import Counter
def char_freq(s): return dict(Counter(s))
3️⃣ Invert a Dictionary (Keys ↔ Values)
def invert_dict(d): return {v: k for k, v in d.items()}

✅ DSA Essentials
    • Find First Non-Repeating Character
def first_unique_char(s):
    freq = {}
    for c in s:
        freq[c] = freq.get(c, 0) + 1
    for i, c in enumerate(s):
        if freq[c] == 1:
            return i
    return -1
    • Group Anagrams (Hash Map + Sorting)
from collections import defaultdict
def group_anagrams(words):
    res = defaultdict(list)
    for word in words:
        key = tuple(sorted(word))
        res[key].append(word)
    return list(res.values())
    • Two Sum (Dict Based Lookup)
def two_sum(nums, target):
    seen = {}
    for i, num in enumerate(nums):
        if target - num in seen:
            return [seen[target - num], i]
        seen[num] = i

💡 Pro Tip
⚡ Always use .get(key, default) → avoids KeyError when key is missing.
👉 Example →
d.get('missing_key', 'default_value')
