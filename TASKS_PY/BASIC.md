### **1. Check if a String is a Pangram**

> A pangram contains every letter of the alphabet at least once.

```python
s = "The quick brown fox jumps over a lazy dog"
s = s.lower()
print(set('abcdefghijklmnopqrstuvwxyz').issubset(set(s)))
```

---

### **2. Find All Prime Numbers in a Range**

```python
start, end = 10, 50
for num in range(start, end+1):
    if all(num % i != 0 for i in range(2, int(num**0.5)+1)) and num > 1:
        print(num, end=' ')
```

---

### **3. Generate All Substrings of a String**

```python
s = "abc"
subs = [s[i:j+1] for i in range(len(s)) for j in range(i, len(s))]
print(subs)
```

---

### **4. Group Words that are Anagrams**

```python
words = ["act", "cat", "tac", "dog", "god"]
group = {}
for w in words:
    key = ''.join(sorted(w))
    group.setdefault(key, []).append(w)
print(list(group.values()))
```

---

### **5. Recursively Compute GCD of Two Numbers**

```python
def gcd(a, b):
    return a if b == 0 else gcd(b, a % b)

print(gcd(48, 18))
```

---

### **6. Flatten a Nested List**

```python
def flatten(lst):
    for i in lst:
        if isinstance(i, list):
            yield from flatten(i)
        else:
            yield i

nested = [1, [2, [3, 4], 5], 6]
print(list(flatten(nested)))
```

---

### **7. Find First Non-Repeating Character**

```python
s = "aabbcdeff"
for c in s:
    if s.count(c) == 1:
        print("First non-repeating:", c)
        break
```

---

### **8. Longest Word in a Sentence**

```python
s = "Python is a great programming language"
words = s.split()
print(max(words, key=len))
```

---

### **9. Check Sudoku Row Validity**

```python
row = [5, 3, 4, 6, 7, 8, 9, 1, 2]
print("Valid" if len(set(row)) == 9 else "Invalid")
```

---

### **10. Matrix Transpose**

```python
mat = [[1, 2, 3], [4, 5, 6]]
transpose = [[row[i] for row in mat] for i in range(len(mat[0]))]
print(transpose)
```

---

### **11. Find Missing Number in 1-N**

```python
nums = [1, 2, 3, 5]
n = 5
print("Missing:", n * (n + 1) // 2 - sum(nums))
```

---

### **12. Convert Roman Numeral to Integer**

```python
s = "XIV"
map = {'I': 1, 'V': 5, 'X': 10}
total = 0
prev = 0
for c in reversed(s):
    val = map[c]
    total += val if val >= prev else -val
    prev = val
print(total)
```

---

### **13. Merge Two Sorted Lists**

```python
a, b = [1, 3, 5], [2, 4, 6]
i = j = 0
merged = []
while i < len(a) and j < len(b):
    merged.append(a[i] if a[i] < b[j] else b[j])
    i += a[i] < b[j]
    j += not (a[i-1] < b[j]) if a[i-1] < b[j] else 0
merged += a[i:] + b[j:]
print(merged)
```

---

### **14. Count Character Frequency in a String**

```python
s = "banana"
freq = {}
for c in s:
    freq[c] = freq.get(c, 0) + 1
print(freq)
```

---

### **15. Find Pairs with Given Sum**

```python
nums = [2, 4, 3, 5, 7]
target = 7
seen = set()
for num in nums:
    if target - num in seen:
        print((num, target - num))
    seen.add(num)
```

---

### **16. Recursively Print All Permutations of a String**

```python
def permute(s, path=''):
    if not s:
        print(path)
    for i in range(len(s)):
        permute(s[:i] + s[i+1:], path + s[i])

permute("abc")
```

---

### **17. Rotate List Elements by K Steps**

```python
lst = [1, 2, 3, 4, 5]
k = 2
k %= len(lst)
rotated = lst[-k:] + lst[:-k]
print(rotated)
```

---

### **18. Pascal’s Triangle (N Rows)**

```python
n = 5
for i in range(n):
    row = [1]
    for j in range(1, i):
        row.append(prev[j-1] + prev[j])
    if i > 0:
        row.append(1)
    print(row)
    prev = row
```

---

### **19. Validate Brackets**

```python
s = "{[()]}"
stack = []
pairs = {'(': ')', '{': '}', '[': ']'}
for c in s:
    if c in pairs:
        stack.append(c)
    else:
        if not stack or pairs[stack.pop()] != c:
            print("Invalid")
            break
else:
    print("Valid" if not stack else "Invalid")
```

---

### **20. Calculate Nth Fibonacci Using Memoization**

```python
memo = {0: 0, 1: 1}
def fib(n):
    if n not in memo:
        memo[n] = fib(n-1) + fib(n-2)
    return memo[n]

print(fib(30))
```
