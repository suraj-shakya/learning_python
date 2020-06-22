# Modules

Quiting the Python interpreter and entering it again, will make all your pogress like variables, functions etc lost. For longer program, it is better off writing the program using a text editor and running from a file instead. This process is creating a script.

As your program gets longer, splitting them over a file make more sense for easier maintenance. You may also want to use the program in the file into several programs without cloning its definiton.

A module is basically a file containing all your variables, functions, definitions etc. The file name is the module name with suffix `.py` appended. Within a module, the module's name is vailable as the value of the global variable `__name__`.

```python
# fibo.py
# Fibonacci module

def fib(n):
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a,b = b, a+b
    return result
```

We can import the above module with following statement:

```python
# Import fibo module
import fibo

number = 100
fibo.fib(100)
```

## Modules in detail

A module can contain executable statements as well as function definitions.  They are executed only the first time the module name is encountered in an import statement.

Each module has its own private symbol table, which is used as the global symbol table by all functions defined in the module. Thus, the author of a module can use global variables in the module without worrying about accidental clashes with a user’s global variables. On the other hand, if you know what you are doing you can touch a module’s global variables with the same notation used to refer to its functions, `module.item_name`.

Modules can import other modules. It is customary but not required to place all `import` statements at the beginning of a module (or script, for that matter).

## Different variants of `import`

Import names from a module directly into importing module's symbol table.

```python
from module_a import a
from module_all import a, b
```

Import all names defined in the module:

```python
from module import *
```

In general, practice of importing `*` from a module is not a good idea, as it often causes poorly readable code. You can import with `*` when in interpreter or interactive mode.

Import using `as` will bound the module name directly to the imported module.

```python
import Headphones as JBL

JBL.play('Happy')
```

Import using `as` and `from`

```python
from Headphones import play as pl

pl('Happy')
```

Modules are imported only once, if the changes are to be reflected, You must restart the interpreter. If you are testing a module, you can use `importlib.reload()` to reload the module.

```python
import importlib
from Amazon import HomeTheatre as Sony

importlib.reload(Sony)
```

## Module's `__name__`

Each module has a name and the statements in a module can access the name of the module. 

It is useful when a module is imported first time, the main block in that module is run. When we want to run the block only when module was run by itself and not while it was imported from another module.

### Example:

```python
# name.py

if __name__ == "__main__":
    print("The module is being run by itself")
else:
    print("The module is being imported from another module")
```

Output:

```bash
$ python name.py
The module is being run by itself
$ python
>>> import name
The module is being imported from another module
```

### Another example:

```python
# fibo.py
# Fibonacci module

def fib(n):
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a,b = b, a+b
    return result

if __name__ == "__main__":
	import sys
    fib(int(sys.argv[1]))
```

Output:

```bash
# Run module by itself
$ python fibo.py 50
0 1 1 2 3 5 8
```

```python
# Import module
from fibo import fib

number = 50
fib(50)
```

## Module Search Pattern

Whenever a module is imported, the interpreter first searches for a build-in module with that name. After that, it searches for a file named `module_name.py` in a list of directories given by `sys.path`.

`sys.path` is initialized from these location:

* Directory containing script or current directory when no file is specified
* PYTHONPATH (a list of directory names, with the same syntax as the shell variable `PATH`)
* The installation-dependent default.

## `.pyc` Files

To speed up loading modules, Python caches the compiled version of each module in the `__pycache__` directory under the name `module.*version*.pyc`, where the version encodes the format of the compiled file; it generally contains the Python version number. For example, in CPython release 3.3 the compiled version of spam.py would be cached as `__pycache__/spam.cpython-33.pyc`. This naming convention allows compiled modules from different releases and different versions of Python to coexist.

Python checks the modification date of the source against the compiled version to see if it’s out of date and needs to be recompiled. This is a completely automatic process. Also, the compiled modules are platform-independent, so the same library can be shared among systems with different architectures.

## `dir()` function

The built-in function `dir()` is used to find out which names a module defines. It returns a sorted list of strings:

```python
>>> import fibo
>>> dir(fibo)
['__name__', 'fib']
```

