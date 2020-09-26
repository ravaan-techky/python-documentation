## Python

### collections:

**counter class**
 - Count uniq element from given list. Result is return in the format of tuple.
   Example:
   ```python
    from collections import Counter
    my_list = [1,1,1,2,2,2,2,3,3,3,3,3]
    Counter(my_list)
    str_var = 'Bhushan Patil'
    Counter(str_var)
    statement = 'India is my country and I live in Maharashtra state of India. My Home is in Pune'
    Counter(statement.split())
   ```
   Output:
   ```python
    Counter({1: 3, 2: 4, 3: 5})
    Counter({'B': 1,
        'h': 2,
        'u': 1,
        's': 1,
        'a': 2,
        'n': 1,
        ' ': 1,
        'P': 1,
        't': 1,
        'i': 1,
        'l': 1})
    Counter({'India': 1,
        'is': 2,
        'my': 1,
        'country': 1,
        'and': 1,
        'I': 1,
        'live': 1,
        'in': 2,
        'Maharashtra': 1,
        'state': 1,
        'of': 1,
        'India.': 1,
        'My': 1,
        'Home': 1,
        'Pune': 1})
   ```

**Important method from counter class**

| method name | description |
| --- | --- |
| sum(counter_var.values()) | summation of all values from counter |
| counter_var.clear | reset all counts |
| list(counter_var) | convert counter class instance into list |
| set(counter_var) |  convert counter class instance into set |
| dict(counter_var) |  convert counter class instance into dict |
| counter_var.items() | convert counter class instance key-value pair |
| counter_var.most_common()[:n-1:-1] | n least common elements |
| counter_var += counter()| remove zero and negative counts from result. |

**Differences between defaultdict & dict**
 - When we create dict object with defaultdict class all unavailable key will not throw an error at the time of retriving them.
 Example of creating dictionary from dict -
 ```python
 dict_var = {'a':1, 'b':2, 'c':3}
 print(dict_var['q'])
 ```
 Output -
 ```python
	File "<ipython-input-1-50cdd1217da3>", line 2
		print(dict_var['a'])
		^
	IndentationError: unexpected indent
 ```
  Example of creating dictionary from defaultdict class -
 ```python
	from collections import defaultdict
	dict_var = defaultdict(lambda:0)
	print(dict_var)
	print(dict_var['new_key'])
	print(dict_var)
	dict_var['new_key']=65
	print(dict_var['new_key'])
	print(dict_var)
 ```
 Output -
 ```python
	defaultdict(<function <lambda> at 0x0000020CFD4F33A0>, {})
	0
	defaultdict(<function <lambda> at 0x0000020CFD4F33A0>, {'new_key': 0})
	65
	defaultdict(<function <lambda> at 0x0000020CFD4F33A0>, {'new_key': 65})
 ```
 
 **Differences between tuple & namedtuple**
 - tuples are only accessible through index while namedtuple also accessible through name.
 - In tuples, always need to remember index of elements.
 Example of accessing element from tuple -
 ```python
	tuple_var = (10, 20, 30)
	print(tuple_var[1])
 ```
 Output -
 ```python
	20
 ```
  Example of creating tuple from namedtuple class -
 ```python
	from collections import namedtuple
	Dog = namedtuple('Dog',['age', 'name', 'bread'])
	tommy_dog = Dog(age=3, name='tommy', bread='Huskey')
	print('=======Dog Information=======')
	print(f'Name : {tommy_dog.name}')
	print(f'Bread : {tommy_dog.bread}')
	print(f'Age : {tommy_dog.age}')
 ```
 Output -
 ```python
	=======Dog Information=======
	Name : tommy
	Bread : Huskey
	Age : 3
 ```
 
<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)
