# Some Python Basics

## Multiple files in python

Lets create two files in same folder
```text
my_folder/
    |___ hello.py
    |___ world.py
```

<br/>

- `hello.py`
```py
# Part-1
def sayHello(name):
    print( "Hello", name )

# Part-2
if __name__ == "__main__":
    print("This is hello.py file")
```

<br/>
<br/>

- `world.py`
```py
# Part-1
import hello

# Part-2
hello.sayHello("Tom")        # Hello Tom

# Part-3
if __name__ == "__main__":
    print("This is world.py")
```

<br/>
<br/>
<br/>
<br/>


## Finding the type of a variable

```py
a = 20

type(a)       # <class 'int'>
```