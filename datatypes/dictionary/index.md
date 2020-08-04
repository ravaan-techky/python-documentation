## Python
dictionary data type:

- Unsorted mapping for storing objects.
- dictionary uses key-value pairing.
- We can quickly grab value object with the help by key.
- dictionary use curly braces and colon to specify the keys and their assiciated values.

Example, - 

```markdown
Input =>
my_dict = {"banana":10.00, "apple":30.00, "orange":25.50}
print(my_dict)
Output =>
{"banana":10.00, "apple":30.00, "orange":25.50}
```

### dictionary operations

**Example - 1:**
```markdown
Input =>
my_dict = {"banana":10.00, "apple":30.00, "orange":25.50}
my_dict['apple']
Output =>
30.00
```

**Example - 2:**
```markdown
Input =>
my_dict = {"key1":"a", "key2":"b", "key3":"c"}
my_dict['key2'].upper()
Output =>
B
```

**Example - 3:**
```markdown
Input =>
my_dict = {"k1":"a", "k2":[1, 2, 3], "k3":"c"}
my_dict['k2'][2]
Output =>
3
```

**Example - 4:**
```markdown
Input =>
my_dict = {"username":"jsmith", "detail":{"firstName":"John", "lastName":"Smith", "age":20}}
my_dict['detail']['age']
print(my_dict['detail']['firstName'] + ' ' + my_dict['detail']['lastName'] + ' age is ' + my_dict['detail']['age'])
Output =>
20
John Smith age is 20
```

**Example - 5: Adding element into dictionary**
```markdown
Input =>
my_dict = {"username":"jsmith", "detail":{"firstName":"John", "lastName":"Smith", "age":20}}
my_dict['address'] = 'India'
my_dict['detail']['age'] = 25
my_dict
print(my_dict['detail']['firstName'] + ' ' + my_dict['detail']['lastName'] + ' age is ' + my_dict['detail']['age'])
Output =>
{"username":"jsmith", "detail":{"firstName":"John", "lastName":"Smith", "age":20}, "address": "India"}
John Smith age is 25
```

**Other useful methods:**
```markdown
Input =>
my_dict = {"banana":10.00, "apple":30.00, "orange":25.50}
```

| Method | Usage | Output | Additional Information |
| --- | --- | --- | --- |
| keys | my_dict.keys() | ['banana', 'apple', 'orange'] | Method returns all keys from dictionary |
| values | my_dict.values() | [10.00, 30.00, 25.50] | Method returns all values from dictionary |
| items | my_dict.items() | ("banana":10.00, "apple":30.00, "orange":25.50) | Method returns tuple from dictionary. Tuple is immutuable. not able to re-assigned |

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
