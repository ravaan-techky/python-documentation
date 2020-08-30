## Python

### Python Errors and Exceptions:

```python
BaseException
 +-- SystemExit
 +-- KeyboardInterrupt
 +-- GeneratorExit
 +-- Exception
      +-- StopIteration
      +-- StopAsyncIteration
      +-- ArithmeticError
      |    +-- FloatingPointError
      |    +-- OverflowError
      |    +-- ZeroDivisionError
      +-- AssertionError
      +-- AttributeError
      +-- BufferError
      +-- EOFError
      +-- ImportError
      |    +-- ModuleNotFoundError
      +-- LookupError
      |    +-- IndexError
      |    +-- KeyError
      +-- MemoryError
      +-- NameError
      |    +-- UnboundLocalError
      +-- OSError
      |    +-- BlockingIOError
      |    +-- ChildProcessError
      |    +-- ConnectionError
      |    |    +-- BrokenPipeError
      |    |    +-- ConnectionAbortedError
      |    |    +-- ConnectionRefusedError
      |    |    +-- ConnectionResetError
      |    +-- FileExistsError
      |    +-- FileNotFoundError
      |    +-- InterruptedError
      |    +-- IsADirectoryError
      |    +-- NotADirectoryError
      |    +-- PermissionError
      |    +-- ProcessLookupError
      |    +-- TimeoutError
      +-- ReferenceError
      +-- RuntimeError
      |    +-- NotImplementedError
      |    +-- RecursionError
      +-- SyntaxError
      |    +-- IndentationError
      |         +-- TabError
      +-- SystemError
      +-- TypeError
      +-- ValueError
      |    +-- UnicodeError
      |         +-- UnicodeDecodeError
      |         +-- UnicodeEncodeError
      |         +-- UnicodeTranslateError
      +-- Warning
           +-- DeprecationWarning
           +-- PendingDeprecationWarning
           +-- RuntimeWarning
           +-- SyntaxWarning
           +-- UserWarning
           +-- FutureWarning
           +-- ImportWarning
           +-- UnicodeWarning
           +-- BytesWarning
           +-- ResourceWarning
```

### try-except example (Handling all Exceptions)
```python
try:
    num1 = 10
    num2 = '10'
    add(num1, num2)
except:
    print('Input for add method is not correct')
print('My program is running!!!')
```
Output -
```python
Input for add method is not correct
My program is running!!!
```

*try-except-else block example 1*
```python
try:
    num1 = 10
    num2 = 10
    add(num1, num2)
except:
    print('Input for add method is not correct')
else:
    print('Input for add method is correct')
print('My program is running!!!')
```

Output -
```python
Input for add method is correct
My program is running!!!
```

*try-except-else block example 2*
```python
try:
    num1 = 10
    num2 = '10'
    add(num1, num2)
except TypeError:
    print('Got Type Error')
else:
    print('Input for add method is correct')
print('My program is running!!!')
```
Output -
```python
```

*File operation and OSError exception*
```python
try:
    f = open('textFile.txt', 'r')
    f.write('Hello World, First line of code.')
except OSError:
    print('Failed to write into file.')
finally:
    print('Closing file')
    f.close()
```
Output -
```python
Failed to write into file.
Closing file
```

*try-except-finally with input example 1*
```python
def checkInputAsNumber():
    try:
        inputText = input('Enter valid number :')
        return int(inputText)
    except ValueError:
        print('Failed to convert text to int')
    finally:
        print('Executing finally block')
```
Definition Calling -
```python
checkInputAsNumber()
```
Output -
```python
Enter valid number :12
Executing finally block
12
```
*try-except-finally with input example 2*
```python
def checkInputAsNumber():
    while True:
        try:
            inputText = input('Enter valid number :')
            return int(inputText)
        except ValueError:
            print('Failed to convert text to int')
            continue
        else:
            break
        finally:
            print('Executing finally block')
```
Definition Calling -
```python
checkInputAsNumber()
```
Output - 
```python
Enter valid number :a
Failed to convert text to int
Executing finally block
Enter valid number :d
Failed to convert text to int
Executing finally block
Enter valid number :1
Executing finally block
```
