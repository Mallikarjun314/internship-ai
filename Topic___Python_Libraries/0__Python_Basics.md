# Some Python Basics

<br/>

## Multiple files in python

Lets create two files in same folder
```text
my_folder/
    |___ hello.py
    |___ my_code.py
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
```py
# Part - 1
import hello

# Part - 2
hello.sayHello("Tom")        # Hello Tom
```

<br/>
<br/>

- Lets run `my_code.py` file and see the output

`python   my_code.py`

<br/>
<br/>
<br/>


## Finding the type of a variable

<br/>
<br/>

- Builtin Types - `int`, `str`, `bool`, `dict`, `list`

```py
a = 20

type(a)       # <class 'int'>
```


<br/>
<br/>

- Custome Types - By using `class` keyword

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