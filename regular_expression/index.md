## Python
### Regular Expression
 - Python regular expression module available in re package.
 
 - Special characters used in regular expression, - 
 
 | Character | Description | Example pattern code | Example match |
 | --- | --- | --- | --- |
 | \d | A digit | file_\d\d | file_24 |
 | \w | Aplhanumeric (Also include underscore characters in match) | \w-\w\w\w | A-b_1 |
 | \s | Whilespace | a\sb\s\c | a b c |
 | \D | A non digit | \D\D\D\D | aBcD |
 | \W | Non-alphanumeric | \W\W\W\W\W | *_+=) |
 | \S | Non-whitespace | \S\S\S\S | Yoyo |

- Occurences related special characters, -

 | Character | Description | Example pattern code | Example match |
 | --- | --- | --- | --- |
 | + | Occurs one or more times | Version \w-\w+ | Version A-B_1 |
 | {3} | Occurs three times | \D{3} | 123 |
 | {2,4} | Occurs 2 to 4 times | \d{2,4} | 123 |
 | {3,} | Occurs 3 or more times | \w{3,} | sdaw3rfwe4 |
 | * | Occurs zero or more times | ABC* | AAACCC |
 | ? | Occur Once or None | plurals? | plural |

 - Condition based regular expression characters, -
 
 | Character | Description | Example pattern code | Example match |
 | --- | --- | --- | --- |
 | pipe sign | OR condition in regular expression | r'cat|dog' | Statement 1: This is a dog! <br/>Statement 2: This is a cat! |
 | . (wild char) | period sign indicate wild char for get given position | r'...at' | Statement : The cat in the hat went splat <br/> Result will be - ['e cat', 'e hat', 'splat'] | 
 | ^ (power sign) | First occurence should match with pattern | r'^\d' | Statement : 2 is Number. <br/> Result will be - [2] | 
 | $ (dollar sign) | Last occurence should match with pattern | r'$\d' | Statement : The Number is 2 <br/> Result will be - [2] | 

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

**Multiple Regular Expression with OR condition (PIPE separator) example:**

Input:
```python
import re
friend_name = 'Harshal'
statement = f'{friend_name} is my friend and He is my best friend and his contact detail is 838-009-3898'
pattern = re.compile('Abhay|Harshal|Sanjay|Abhijeet')
search_result = re.search(pattern, statement)
if search_result != None:
    print(f'Result found with start index {search_result.start()} and end index {search_result.end()}')
    print(f'Available friend is {search_result.group()}')
else:
    print('No result found!')
```
Output:
```python
Result found with start index 0 and end index 7
Available friend is Harshal
```

**Wild char Regular Expression (period sign) example:**

Input:
```python
import re
friend_name = 'Sanket'
statement = f'{friend_name} is my friend and He is my good friend and his contact detail is 838-009-3898'
pattern = re.compile('my......friend')
search_result = re.search(pattern, statement)
if search_result != None:
    print(f'Result found with start index {search_result.start()} and end index {search_result.end()}')
    print(f'Available friend is {search_result.group()}')
else:
    print('No result found!')
```
Output:
```python
Result found with start index 30 and end index 44
Available friend is my good friend
```

**Exclusion operation with Regular Expression example:**

```python
import re
#exclusion syntax with the help of regular expression
statement = 'there are 3 numbers 34 inside 5 this sentence'
pattern = r'[^\d]'  # Generate list of characters from above statement
pattern = r'[^\d]+' # Generate list of words which gets separated with number
re.findall(pattern, statement)
```

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
