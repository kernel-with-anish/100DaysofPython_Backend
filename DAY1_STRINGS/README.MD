🚀 Day 01 – Python Strings

✅ What’s a String?
Immutable sequence of characters → "Hello World" | 'Python Rocks' | """Multi-line"""

⚡ Syntax Cheatsheet
# Access & Slicing
s = "Python"
s[0], s[-1], s[1:4], s[::-1]

# Common Methods
s.upper(), s.lower(), s.strip(), s.replace('Py', 'Ja'), ' '.join(['Py', 'is', 'fun'])

# f-string
name = "Anish"
f"Hello, {name}"

✔️ Key Concepts
    • Immutable → No in-place changes.
    • Escape chars → \n, \t, \\
    • Efficient concat → ' '.join(list) ≫ + in loops
    • Membership → 'Py' in s → True

⚡ Problems to Master
1️⃣ Reverse String (Manual)
def reverse(s): return ''.join(reversed(s))
2️⃣ Palindrome Check
def is_palindrome(s):
    s = ''.join(filter(str.isalnum, s)).lower()
    return s == s[::-1]
3️⃣ Word Count
def word_count(s): return len(s.strip().split())

✅ DSA Essentials
    • Longest Unique Substring (Sliding Window)
def longest_unique(s):
    seen, l, res = set(), 0, 0
    for r in range(len(s)):
        while s[r] in seen:
            seen.remove(s[l]); l += 1
        seen.add(s[r])
        res = max(res, r - l + 1)
    return res
    • Anagram Check
from collections import Counter
def is_anagram(s1, s2): return Counter(s1) == Counter(s2)
    • Valid Parentheses
def valid_parentheses(s):
    stack, mapping = [], {')':'(', ']':'[', '}':'{'}
    for c in s:
        if c in mapping:
            if not stack or stack.pop() != mapping[c]: return False
        else:
            stack.append(c)
    return not stack

💡 Pro Tip
Always prefer .join(list) for concat → faster, cleaner, and less memory waste.

