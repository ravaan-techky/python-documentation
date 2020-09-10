## Python

### Generator:
- Only returning value which requires operation and keep track of previous value to compute next value.
- Memory Usage is optimum than List.
- Could be use in less hardware configuration.

### Example
- Creating simple function which returning cube of given number
```python
def get_cube(n):
	result = []
	for t in range(n):
		result.appen(t**3)
	return result
```
Input:
```python
	get_cube(5)
```
Output:
```python
[0, 1, 8, 27, 64]
```
Input:
```python
	result = get_cube(5)
	for number in result:
		print(number)
```
Output:
```python
0
1
8
27
64
```
In above get_cube function, we are creating result array and then returning it from function.

```python
def get_cube(n):
	for t in range(n):
		yield t
```

Input:
```python
	get_cube(5)
```
Output:
```python
<generator object get_cube at 0x000002B219DFF660>
```
Input:
```python
	result = get_cube(5)
	for number in result:
		print(number)
```
Output:
```python
0
1
8
27
64
```
 In above get_cube function, we are not creating result array and generate one value at a time.
 
 ### next function
 On Generator object we can use next function to return next value from result.
 Example, - 
 ```python
 def get_cube(n):
    for num in range(n):
        yield num **3
 ```
 Input:
 ```python
 res = get_cube(5)
 print(next(res))
 print(next(res))
 print(next(res))
 ```
 Output:
 ```python
 0
 1
 8
 ```
 
 next function give error in case if object is not type of generator
 Example, - 
 ```python
def get_cube(n):
    result = []
    for num in range(n):
        result.append(num ** 3)
    return result
 ```
 Input:
 ```python
 res = get_cube(5)
 print(next(res))
 ```
 Output:
 ```python
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-9-99bd7a0c47e0> in <module>
----> 1 next(res)

TypeError: 'list' object is not an iterator
 ```
 
 To provide 'list' object an iterator, we can use iter method
  Example, - 
 ```python
def get_cube(n):
    result = []
    for num in range(n):
        result.append(num ** 3)
    return result
 ```
 Input:
 ```python
 res = get_cube(5)
 new_res = iter(res)
 print(next(new_res))
 print(next(new_res))
 print(next(new_res))
 ```
  Output:
 ```python
 0
 1
 8
 ```
 
<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/documentation/)
