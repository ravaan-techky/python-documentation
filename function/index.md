## Python

### Functions in pythons:

**Creating function:**
```python
def function_name():
    '''
       Documentation regarding function work and parameter information
    '''
    #Function operation implementation
```

|keyword | Details |
| --- | --- |
| def | definition of function. |
| function_name | Function name. Snake casing is use as standard for function name. (Snake casing is all character is in lower letter and connected with spaces |
| : | A colon indicate upcoming intended block is implementation for function. |
| ''' Documentation ''' | Documentation regarding function work and parameter information |

**args (Variable argument list) keywords:**

Function Decalaration:
```python
def average(*args):
    '''
       Average function. Taking number as args input and return their average
    '''
    return sum(args) / len(args)
```

Calling example, - 
```python
  print(f'Total Average for (1, 2, 3, 4, 5) is : {average((1, 2, 3, 4, 5))}')
```

**kargs (Key-Value Paired argument) keyword:**

Function Decalaration:
```python
def showStudentInformation(**kargs):
    '''
       show student information function show student name, address, marks and Percentage
    '''
    print(f'========== Student Information ==========')
    print(f'Name         : {kargs["name"]}')
    print(f'Address      : {kargs["address"]}')
    print(f'Marks        : {kargs["marks"]}')
    print(f'Percentage   : {(sum(kargs["marks"]) / len(kargs["marks"])) * 100.00}')
```

Calling example, - 
```python
  showStudentInformation({'name:'John Simth', 'address': 'Pune', 'marks':[120,140,130]})
```

**map built-in function**

- Map modifies the list with a normal logic that produces another list

```python
# square method
def square(num):
    return num ** 2
```

```python
#Map to return square of each element of list.
print(map(square, [1, 2, 3, 4, 5]))
squareList = list(map(square, [1, 2, 3, 4, 5]))
print(squareList)
```

```
Output => [1, 4, 9, 16, 25]
```

**filter built-in function**

- Filter modifies the list with conditional logic that filters out some elements
```python
#is even number function
def isEvenCheck(num):
    return num ** 2
```

```python
#Filter to find out even number from list
print(filter(isEvenCheck, [1, 2, 3, 4, 5, 6]))
evenList = list(filter(isEvenCheck, [1, 2, 3, 4, 5, 6]))
print(evenList)
```

```
Output => [2, 4, 6]
```


**lambda keyword**

-syntax
```python
    square = lambda num : num ** 2
```

|keyword | Details |
| --- | --- |
| square | variable name |
| lambda | lambda keyword |
| num | Input variable |
| : | A colon indicate upcoming intended block is implementation for function. |
| num ** 2 | method body |

Example-1 Converting above mentioned square function into lambda expression, -
```python
myNumList = [1,2,3,4,5,6]
mySquareList = list(map(lambda num: num ** 2, myNumList))
mySquareList
```
Output:
```
[1, 4, 9, 16, 25, 36]
```

Example-2 Converting above mentioned isEven function into lambda expression, -
```python
myNumList = [1, 2, 3, 4, 5, 6]
myEvenList = list(filter(lambda num: num % 2 == 0, myNumList))
myEvenList
```
Output:
```
[2, 4, 6]
```

Example-3 Reverse string of list, -
```python
myNameList = ['Bhushan', 'Sandip', 'Neel', 'Lavanya', 'Nidhi']
myResultList = list(map(lambda name: name[::-1], myNameList))
myResultList
```
Output:
```
['nahsuhB', 'pidnaS', 'leeN', 'aynavaL', 'ihdiN']
```


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)
