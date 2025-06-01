# Most used Python data types

| Category  | Data Type                 |
| --------- | ------------------------- |
| Text      | `str`                     |
| Numeric   | `int`, `float`, `complex` |
| Boolean   | `bool`                    |
| None Type | `NoneType`                |
| Sequence  | `list`, `tuple`           |
| Mapping   | `dict`                    |
| Set       | `set`, `frozenset`        |

\
\
\
.

### Python Keywords, Usage Examples

```py
# Integer 
a = int("23")
print(a)                    # Output: 23
print(type(a))              # Output: <class 'int'>



# Float 
b = float("2.34")
print(b)                    # Output: 2.34
print(type(b))              # Output: <class 'float'>



# complex number 
c = 3 + 4j
print(b)                    # Output: (3+4j)
print(type(b))              # Output: <class 'complex'>



# Boolean
d = True
print(d)                    # Output: True
print(type(d))              # Output: <class 'bool'>



# Valid String syntax
# All these are valid string syntax
s1 = "Hello Hello"
s2 = 'Hello World'
s3 = """Hello World"""
s4 = '''Hello World'''
print(s1)                   # Output: "Hello World"
print(type(s1))             # Output: <class 'str'>



# list - Mutable
e = [1,2,3,4,5]
print(e)                    # Output: [1, 2, 3, 4, 5]
print(type(e))              # Output: <class 'list'>



# Tuple - Immutable 
f = (1,2,3,4)
print(e)                    # Output: (1, 2, 3, 4)
print(type(e))              # Output: <class 'tuple'>



# Dictionary 
g = {
    "hello" : {
        "world" : 123
    },
    "a boolean value": True,
    "Digits": [0,1,2,3,4,5,6,7,8,9],
    "Marks": {
        "Maths": 90,
        "Social": 80,
        "Science": 85,
    }
}
print(g["hello"]["world"])              # Output: 123
print(g["a boolean value"]["world"])    # Output: True
print(g["Digits"][2])                   # Output: 2
print(type(g))                          # Output: <class 'dict'>



# Set - Mutable 
h = set({1,2,3,3,4,5,4})
print(h)                        # Output: {1, 2, 3, 4, 5}
print(type(h))                  # Output: <class 'set'>



# Frozen Set - Immutable
i = frozenset({1,2,3,3,4,5,4})
print(i)                        # Output: frozenset({1, 2, 3, 4, 5})
print(type(i))                  # Output: <class 'frozenset'>

```