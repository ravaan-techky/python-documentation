## Python
### Regular Expression
 - Python regular expression module available in re package.

**in keyword example:**
Input:
```python
my_var = 'bhushan' in 'bhushan is my name'
print(my_var)
```
Output:
```python
True
```

**Regular Expression search function example:**
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

**Regular Expression findall function example:**
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

**Regular Expression finditer function example:**

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


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
