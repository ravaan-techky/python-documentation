## Python

### Logical operator:

| Operator | Example | Description |
| --- | --- | --- |
| and | Input: 1 == 1 and 2 < 4 <br/>Output: True <br/>Input: 1 == 1 and 2 != 2 <br/>Output: False | Both condition must True. |
| or | Input: 1 == 1 or 2 < 4 <br/>Output: True <br/>Input: 1 == 1 or 2 != 2 <br/>Output: True | One of the condition from both must True. |
| not | Input: not 1 != 2 <br/>Output: True <br/>Input: not 1 == 1 <br/>Output: False | Negection of actual result. |

### IF, ELIF and ELSE statement:

 - Syntax of an IF statement
 ```python
	if some_condition :
		# execute_some_condition
 ```
 - Syntax of an IF ELSE statement
 ```python
	if some_condition :
		# execute_some_condition
	else :
		# do something else
 ```
 - Syntax of an IF ELIF ELSE statement
 ```python
	if some_condition :
		# execute_some_condition
	elif some_other_condition :
		# do something different
	else :
		# do something else
 ``` 

### FOR LOOP statement:
 - Syntax of an FOR LOOP statement
 ```python
	 myList = [1, 2, 3, 4, 5]
	 for item in myList:
		print(item)
 ```
 
 **Example**
  ```python
	# Iterating to print element from list.
	myList = [1, 2, 3, 4, 5]
	for item in myList:
		print(item)
	Output:
	1
	2
	3
	4
	5

	# Iterating to print characters from Hello string.
	for item in 'Hello':
		print(item)
	Output:
	H
	e
	l
	l
	0

	# Iterating to print value from tuple object.
	tupleVar = (1, 2, 3, 4)
	for value in tupleVar:
		print(value)
	Output:
	1
	2
	3
	4
 ```
 **tuples packing and unpacking using FOR LOOP**
 
 **tuple Example** 
 ```python
	myList = [(1, 2), (3, 4), (5, 6)]
	for tupleValues in myList:
		print(tupleValues)
	Output:
	(1, 2)
	(3, 4)
	(5, 6)
	
	for a, b in myList:
		print(a)
		print(b)
	Output:
	1
	2
	3
	4
	5
	6
 ```
 **dictionary Example** 
 ```python
	myDict = {'name': 'John', 'email': 'john@gmail.com', 'address': 'Pune' }
	#Printing all keys from dictionary.
	for item in myDict:
		print(item)
	Output:
	name
	email
	address

	#Printing all key and value from dictionary.
	for item in myDict.items():
		print(item)
	Output:
	('name', 'John')
	('email', 'john@gmail.com')
	('address', 'Pune')

	#Printing all key and value from dictionary.
	for key, value in myDict.items():
		print('key {} value is {}'.format(key, value))
	Output:
	key name value is John
	key email value is john@gmail.com
	key address value is Pune
	
	#Printing all value from dictionary.
	for value in myDict.values():
		print(value))
	Output:
	John
	john@gmail.com
	Pune
 ```
 
 ### WHILE LOOP statement:
 
 **syntax**
 ```python
	while some_condition:
		//do something
	else:
		//do something different
 ```
 
**Example 1**
```python
	num = 0
	while num < 5:
		print('Number {}'.format(num))
		num += 1
	Output:
	Number 0
	Number 1
	Number 2
	Number 3
	Number 4
```

**Example 2**
```python
	num = 0
	while num < 5:
		print('Number {}'.format(num))
		num += 1
	else:
		print('Number is greater than 5')
	Output:
	Number 0
	Number 1
	Number 2
	Number 3
	Number 4
	Number is greater than 5
```

### break, continue and pass statements in LOOP:

We can use break, continue and pass statements in our loop to add additional functionality for various cases.

| Statement | Description |
| --- | --- |
| break | Breaks out of the current closest enclosing loop |
| continue | Goes to the top of the closest enclosing loop |
| pass | does nothing at all |


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
