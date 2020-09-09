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
 
<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/documentation/)
