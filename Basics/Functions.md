# Functions

- Group/blocks of statements/expressions
- executes only when called
- can be declared with parameters so that desired arguments can be passed
- can return values
- defined by ```def``` keyword
- Signature  
```def <function name>([parameter list if needed]):```  
    ```    <statements>```
     


```python
def printMyName():
    print("hello Falano")

printMyName()
```

    hello Falano
    


```python
# Passing Arguments:
def welcomeFalano(fname):
    print("Welcome {name}!! \nHave a great day".format(name=fname))

name = input("Enter your name")
welcomeFalano(name)
```


```python
#Calling a function without argument but expects one
welcomeFalano()
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-9-769a1e4c164e> in <module>
          1 #Calling a function without argument but expects one
    ----> 2 welcomeFalano()
    

    TypeError: welcomeFalano() missing 1 required positional argument: 'fname'



```python
def welcomePerson(lname, fname):
    print("Welcome {name} {lname}!! \nHave a great day".format(name=fname,lname=lname))

welcomePerson("Shakya","Suraj")
welcomePerson(fname="Suraj",lname="Shakya")

```

    Welcome Suraj Shakya!! 
    Have a great day
    Welcome Suraj Shakya!! 
    Have a great day
    


```python
# Unknown number of arguments
# Also known as arbitary arguments *arguments
# here the argument will be a tuple
def showMyInfo(*info):
    for i in info:
        print(i)
```


```python
showMyInfo("Falano","Manche","Male","Nepal","Nepali")
```

    Falano
    Manche
    Male
    Nepal
    Nepali
    


```python
# Keyword Arguments
# arguments when passed by specifying the key
def printFullName(lname, fname):
    print("{firstname} {lastname}".format(firstname=fname, lastname=lname))

printFullName(fname="Suraj",lname="Shakya")
```

    Suraj Shakya
    


```python
# Arbitary Keyword arguments
# If number of keyword arguments that will be passed is unknown
# here the argument will be of dictionary type
def printFullName(**name):
    for i,v in name.items():
        print("{n}".format(n=v),end=" ")

printFullName(fname="Suraj",lname="Shakya")
```

    Suraj Shakya 

## Special parameters  
By default, arguments may be passed to a Python function either by position or explicitly by keyword. For readability and performance, it makes sense to restrict the way arguments can be passed so that a developer need only look at the function definition to determine if items are passed by position, by position or keyword, or by keyword.

A function definition may look like:  

```def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):```----------- ---------- ---------- | | | | Positional or keyword | | - Keyword only -- Positional only
where / and * are optional. If used, these symbols indicate the kind of parameter by how the arguments may be passed to the function: positional-only, positional-or-keyword, and keyword-only. Keyword parameters are also referred to as named parameters.

### Positional-or-Keyword Arguments  
If / and * are not present in the function definition, arguments may be passed to a function by position or by keyword.

### Positional-Only Parameters  
The / is used to logically separate the positional-only parameters from the rest of the parameters. If there is no / in the function definition, there are no positional-only parameters.

### Keyword-Only Arguments  
To mark parameters as keyword-only, indicating the parameters must be passed by keyword argument, place an * in the arguments list just before the first keyword-only parameter.

#### Examples:


```python
def standard_arg(arg):
    print(arg)
```

The first function definition, standard_arg, the most familiar form, places no restrictions on the calling convention and arguments may be passed by position or keyword:


```python
standard_arg(2)
```

    2
    


```python
standard_arg(arg=2)
```

    2
    


```python
def pos_only_arg(arg,/):
    print(arg)
```

The second function pos_only_arg is restricted to only use positional parameters as there is a / in the function definition:


```python
pos_only_arg(1)
```

    1
    


```python
pos_only_arg(arg=1)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-9-434db44f4ff9> in <module>
    ----> 1 pos_only_arg(arg=1)
    

    TypeError: pos_only_arg() got some positional-only arguments passed as keyword arguments: 'arg'



```python
def kwd_only_arg(*, arg):
    print(arg)
```


```python
kwd_only_arg(3)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-12-896c53ef896c> in <module>
    ----> 1 kwd_only_arg(3)
    

    TypeError: kwd_only_arg() takes 0 positional arguments but 1 was given



```python
kwd_only_arg(arg=3)
```

    3
    


```python
def combined_example(pos_only, /, standard, *, kwd_only):
    print(pos_only, standard, kwd_only)
```

And the last uses all three calling conventions in the same function definition:


```python

combined_example(1, 2, 3)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-15-037a05a37207> in <module>
    ----> 1 combined_example(1, 2, 3)
    

    TypeError: combined_example() takes 2 positional arguments but 3 were given



```python
combined_example(1, 2, kwd_only=3)
```

    1 2 3
    


```python
combined_example(1, standard=2, kwd_only=3)
```

    1 2 3
    


```python
combined_example(pos_only=1, standard=2, kwd_only=3)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-18-a0fe0f8338e9> in <module>
    ----> 1 combined_example(pos_only=1, standard=2, kwd_only=3)
    

    TypeError: combined_example() got some positional-only arguments passed as keyword arguments: 'pos_only'


## Lambda Expressions  

Small anonymous functions can be created with the lambda keyword. This function returns the sum of its two arguments: ```lambda a, b: a+b```. Lambda functions can be used wherever function objects are required. They are syntactically restricted to a single expression. Semantically, they are just syntactic sugar for a normal function definition. Like nested function definitions, lambda functions can reference variables from the containing scope:

### Syntax : 

```lambda arguments : expression```


```python
sum = lambda a: a + 10
print(sum(5))
```

    15
    

### Lambda functions can take any number of arguments :  
A lambda function that multiples argument a with argument b and c and print the result:


```python
multiple = lambda a, b, c : a*b*c
print(multiple(10,20,30))
```

    6000
    

### Why Use Lambda Functions?
The power of lambda is better shown when used as an anonymous function inside another function.

Lets say a function definition takes one argument, and that argument will be multiplied with an unknown number:



```python
def unknownMultiple(n):
  return lambda a : a * n

doubler = unknownMultiple(2)
tripler = unknownMultiple(3)

print(doubler(20))
print(tripler(20))
```

    40
    60
    
