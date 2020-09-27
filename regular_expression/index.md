## Python
### Regular Expression
 - Python regular expression module available in re package.

**IN keyword example:**
Input:
```python
my_var = 'bhushan' in 'bhushan is my name'
print(my_var)
```
Output:
```python
True
```

**Simple Expression search function example:**
Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"
pattern = 'NO PATTERN SET'
re.search(pattern, my_statement)
```
Output: No output will be available. If we try to print output it will be None type

Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"

#return first find object from statement.
pattern = 'phone'
re.search(pattern, my_statement)
```
Output:
```python
<re.Match object; span=(17, 22), match='phone'>
```
Methods from Match object

| Method | Description |
| --- | --- |
| span() | return start and end attribute of first match in tuple |
| start() | return start index |
| end() | return end index |
| group() | return search text |

Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"

#return first find object from statement.
pattern = 'phone'
match = re.search(pattern, my_statement)
print(match.span())
print(match.start())
print(match.end())
print(match.group())
```
Output:
```python
(17, 22)
17
22
phone
```

**Simple Expression findall function example:**
Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"

#return first find object from statement.
pattern = 'phone'
match_list = re.findall(pattern, my_statement)
print(f'Total search count : {len(match_list)}')
print(f'Search Text        : {match_list}')
for (index, match) in enumerate(match_list):
    print(f'Search Number {index}')
    print(f'\t\t found at: {match}')
```
Output:
```python
Total search count : 2
Search Text        : ['phone', 'phone']
Search Number 0
		 found at: phone
Search Number 1
		 found at: phone
```

**Simple Expression finditer function example:**

Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"

#return first find object from statement.
pattern = 'phone'
for match in re.finditer(pattern, my_statement):
    print(f'{match.group()} found at: {match.start()}, {match.end()}')
```
Output:
```python
phone found at: 17, 22
phone found at: 78, 83
```

**Note: finditer function iterate over match object while findall function return only occurences**

**Regular Expression search function example:**
Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"

#return first find object from statement.
pattern = r'\W\d{3}\W-\d{3}-\d{4}'
for match in re.finditer(pattern, my_statement):
    print(f'{match.group()} found at: {match.start()}, {match.end()}')
```
Output:
```python
(999)-999-9999 found at: 30, 44
```

**Regular Expression compile and search function example:**
compile function from re package compile regular expression and divide it into groups. For this purpose it uses open and closing brackets.

Input:
```python
import re
my_statement = "Agent Hitman has phone Number (999)-999-9999 You can call at any time on this phone number!!!"

#return first find object from statement.
pattern = re.compile('\W(\d{3})\W-(\d{3})-(\d{4})') #Each open and closing bracket represent group.
result = re.search(pattern, my_statement)
print(result.span())
print(f'Group 1 {result.group(1)}')
print(f'Group 2 {result.group(2)}')
print(f'Group 3 {result.group(3)}')
print(f'Group 4 {result.group(4)}') # ==> Generate Error as there is no 4th group available
```
Output:
```python
(30, 44)
Group 1 999
Group 2 999
Group 3 9999
```


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
