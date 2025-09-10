🚀 Day 03 – Python Tuples

✅ What’s a Tuple?
An ordered, immutable collection of items → (1, 'Python', 3.14, True)

⚡ Syntax Cheatsheet
# Create Tuples
t1 = (1, 2, 3)
t2 = ('a', 'b', 'c')
t3 = (1,)         # Single element tuple – comma is mandatory
t4 = tuple([1,2,3])  # From list

# Access Elements
t1[0], t1[-1], t1[1:3], t1[::-1]

# Tuple Packing & Unpacking
a, b, c = (1, 2, 3)
packed = 1, 'Py', 3.14

✔️ Key Concepts
    • Immutable → Once created, cannot change (no append(), remove(), etc.).
    • Faster than lists → Useful when data doesn’t change.
    • Supports nesting → t = (1, (2,3), 4) → t[1][1] → 3
    • Hashable → Can be used as dict keys → d = {(1,2): 'tuple key'}

⚡ Problems to Master
1️⃣ Count Elements in Tuple
def count_elements(t): return len(t)
2️⃣ Find Index of Element
def element_index(t, val): return t.index(val)
3️⃣ Convert Tuple to List & Back
def tuple_to_list(t): return list(t)
def list_to_tuple(l): return tuple(l)

✅ DSA Essentials
    • Unpacking Swap Trick
a, b = 5, 10
a, b = b, a  # Swap without temp variable
    • Fixed-size Data Containers (Useful in configs)
config = ('localhost', 8080, 'user', 'pass')
host, port, username, password = config
    • Use Tuples for Immutable Records
coordinates = (12.9716, 77.5946)

💡 Pro Tip
⚡ Use Tuples when data should never change → Faster, safer, and hashable (great for dict keys).
👉 Best for fixed configs, coordinates, return multiple values.
