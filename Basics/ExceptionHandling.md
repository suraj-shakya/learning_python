# Exception Handling 

Python will normally stop and generate an error message in case of any errors/ exceptions. So to handle the unexpected halt of the execution we can use the try- except - finally blocks.

```try
     <<Codes that might have errors>>
   except
     <<handle error>>
   finally
     <<execute code, regardless of the result of the try- and except blocks>>
```


```python
#lets select a statement that will raise an error
print(1/0)
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    <ipython-input-2-458ebdc32137> in <module>
          1 #lets select a statement that will raise an error
    ----> 2 print(1/0)
    

    ZeroDivisionError: division by zero



```python
try:
    print(1/0)
except:
    print("Error has been handled")
finally:
    print("Whatever!!!!")
```

    Error has been handled
    Whatever!!!!
    


```python
try:
    print(1/0)
except ZeroDivisionError:
    print("Known exception: Zero Division Error")
except:
    print("I don't know what happened, but there are exception")
finally:
    print("Whatever!!!!")
```

    Known exception: Zero Division Error
    Whatever!!!!
    


```python
try:
    print(1/0)
except ZeroDivisionError:
    print("Known exception: Zero Division Error")
except:
    print("I don't know what happened, but there are exception")
else:
    print("No errors were found")
finally:
    print("Whatever!!!!")
```

    Known exception: Zero Division Error
    Whatever!!!!
    


```python
try:
    print(1/1)
except ZeroDivisionError:
    print("Known exception: Zero Division Error")
except:
    print("I don't know what happened, but there are exception")
else:
    print("No errors were found")
finally:
    print("Whatever!!!!")
```

    1.0
    No errors were found
    Whatever!!!!
    

## Raise an exception
---
What if manually exception must be raised ???  
use ```raise``` keyword


```python
if 1<2:
    raise Exception("Sorry!!! 1 is less than 2 :D")
    
```


    ---------------------------------------------------------------------------

    Exception                                 Traceback (most recent call last)

    <ipython-input-9-10c85db0fab9> in <module>
          1 if 1<2:
    ----> 2     raise Exception("Sorry!!! 1 is less than 2 :D")
          3 
    

    Exception: Sorry!!! 1 is less than 2 :D



```python
# or any other type of exception
if 0<1:
    raise ZeroDivisionError("Sorry!!! 0 is less than 1 :D")
    
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    <ipython-input-12-69833ca175c4> in <module>
          1 # or any other type of exception
          2 if 0<1:
    ----> 3     raise ZeroDivisionError("Sorry!!! 0 is less than 1 :D")
          4 
    

    ZeroDivisionError: Sorry!!! 0 is less than 1 :D


There is an option for user-defined function too..

Some of the types ...

| Exception | Description |
|:---|:---|
|  AssertionError | Raised when an assert statement fails | 
|  AttributeError | Raised when attribute reference or assignment fails | 
|  Exception | Base class for all exceptions | 
|  EOFError | Raised when the input() method hits an "end of file" condition (EOF) | 
|  ArithmeticError | Raised when an error occurs in numeric calculations | 
|  FloatingPointError | Raised when a floating point calculation fails | 
|  GeneratorExit | Raised when a generator is closed (with the close() method) | 
|  ImportError | Raised when an imported module does not exist | 
|  IndentationError | Raised when indendation is not correct | 
|  IndexError | Raised when an index of a sequence does not exist | 
|  KeyError | Raised when a key does not exist in a dictionary | 
|  KeyboardInterrupt | Raised when the user presses Ctrl+c, Ctrl+z or Delete | 
|  LookupError | Raised when errors raised cant be found | 
|  MemoryError | Raised when a program runs out of memory | 
|  NameError | Raised when a variable does not exist | 
|  NotImplementedError | Raised when an abstract method requires an inherited class to override the method | 
|  OSError | Raised when a system related operation causes an error | 
|  OverflowError | Raised when the result of a numeric calculation is too large | 
|  ReferenceError | Raised when a weak reference object does not exist | 
|  RuntimeError | Raised when an error occurs that do not belong to any specific expections | 
|  StopIteration | Raised when the next() method of an iterator has no further values | 
|  SyntaxError | Raised when a syntax error occurs | 
|  TabError | Raised when indentation consists of tabs or spaces | 
|  SystemError | Raised when a system error occurs | 
|  SystemExit | Raised when the sys.exit() function is called | 
|  TypeError | Raised when two different types are combined | 
|  UnboundLocalError | Raised when a local variable is referenced before assignment | 
|  UnicodeError | Raised when a unicode problem occurs | 
|  UnicodeEncodeError | Raised when a unicode encoding problem occurs | 
|  UnicodeDecodeError | Raised when a unicode decoding problem occurs | 
|  UnicodeTranslateError | Raised when a unicode translation problem occurs | 
|  ValueError | Raised when there is a wrong value in a specified data type | 
|  ZeroDivisionError | Raised when the second operator in a division is zero | 

