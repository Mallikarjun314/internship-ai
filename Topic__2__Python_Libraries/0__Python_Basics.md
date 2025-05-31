# Some Python Basics

<br/>

## 1. Multiple files in python

<br/>
<br/>


### Example 1

Lets create two files in same folder
```text
📂 my_folder_1/
    |
    |___ 📃 hello.py
    |
    |___ 📃 my_code.py
```

<br/>
<br/>

- `hello.py`
```py
# Part - 1
def sayHello(name):
    print( "Hello", name )
```

<br/>
<br/>

- `my_code.py`

1

```py
# Part - 1
import hello

# Part - 2
hello.sayHello("Tom")        # Hello Tom
```

<br/>

2

```py
# Part - 1
import hello as h

# Part - 2
h.sayHello("Tom")        # Hello Tom
```

<br/>

3

```py
# Part - 1
from hello import sayHello

# Part - 2
sayHello("Tom")        # Hello Tom
```

<br/>
<br/>
<br/>

- Lets run `my_code.py` file and see the output

`python   my_code.py`

<br/>
<br/>

| keyword  | Purpose        |
| -------- | -------------- |
| `from`   | Module path    |
| `import` | What to import |
| `as`     | Shorter-name   |

<br/>
<br/>

### Example 2

Lets create two files in same folder

```text
📂 my_folder_2/
    |
    |____ 📂 abcd/
    |     |
    |     |____ 📂 xyz/
    |     |     |
    |     |     |____ 📃 hi.py
    |     |   
    |     |____ 📃 hello.py
    |
    |___ 📃 my_code.py
```

<br/>
<br/>

- `hello.py`
```py
# Part - 1
def sayHello(name):
    print( "Hello", name )
```

<br/>
<br/>

- `hi.py`
```py
# Part - 1
def sayHi(name):
    print( "Hiiii", name )
```


<br/>
<br/>

- `my_code.py`
```py
# Part - 1
from abcd import hello

# Part - 2
from abcd.xyz import hi

# Part - 3
hello.sayHello( "Tom" )        # Hello Tom

# Part - 4
hi.sayHi( "Jerry" )            # Hiii Jerry
```

<br/>
<br/>

- Lets run `my_code.py` file and see the output

`python   my_code.py`

<br/>
<br/>
<br/>



## 2. Finding the type of a variable

<br/>
<br/>

### Builtin Types 

- `int`, `str`, `bool`, `dict`, `list`

```py
a = 20

type(a)       # <class 'int'>
```


<br/>
<br/>

### Custome Types 

- By using `class` keyword

```py
# Part - 1
class Person:

    def __init__(self, name, age):
        self.name = name
        self.age


# Part - 2
p = Person( "Tom", 30 )


# Part - 3
print(type(p))        # <class '__main__.Person'>
```