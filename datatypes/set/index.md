## Python
set datatype:

- unordered collection of unique elements.
- There only be one representative of the same object.
  Example, - 
	```markdown
		my_set = set()
	```

### Set operations

**Adding element into set**
```markdown
Input =>
	my_set = set()
	my_set.add(1);
	print(my_set)
	my_set.add(2);
	print(my_set)
	my_set.add(2);
	print(my_set)
Output =>
	{1}
	{1, 2}
	{1, 2} //No duplicate element is allowed
```

**Adding element into set from list**
```markdown
Input =>
	my_list = [3, 1, 5, 1, 2, 4]
	print(my_list)
	my_set = set(my_list)
	print(my_set)
Output =>
	[3, 1, 5, 1, 2, 4]
	{3, 1, 5, 2}
```

**Adding element into set from string**
```markdown
Input =>
	my_string = 'apple'
	print(my_string)
	my_set = set(my_string)
	print(my_set)
Output =>
	apple
	{'a', 'p', 'l', 'e'}
```


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
