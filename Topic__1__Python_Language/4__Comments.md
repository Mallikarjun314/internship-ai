# Single-line Comments

Simply using `#`

\
\
\
.

# Multi-line Comments (a.k.a Doc Strings)

Writing something in 3 or more quotes (Single`'` or Double`"`)

#### Example :

##### Code:
```py
def sayHello(name):
    """
        This is a functions
        that takes one argument called 'name'
        and prints 'Hello' with that name
    """
    print("Hello", name)


# Calling help on something like a function outputs its documentation
help(sayHello)
```

##### Output :
```
Help on function sayHello in module __main__:

sayHello(name)
    This is a functions
    that takes one argument called 'name'
    and prints 'Hello' with that name
```

