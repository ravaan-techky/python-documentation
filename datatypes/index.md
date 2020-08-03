## Python
Python Datatypes

Python supports **Dynamic Type Bindings**. That means, - we can declare variable with one datatype and 
change type of value on next line. 

Example, - 
 ```markdown
  myString = 10
  print("Number value from myString variable - " + myString)
  myString = "Ten"
  print("String value from myString variable - " + Ten)
 ```
*Pros of Dynamic Type Bindings:*
- Very easy to work with
- Faster development time.

*Cons of Dynamic Type Bindings:*
- May result in *bugs* for unexcepted data types!
- you need to be aware of type()

### Available data types:

| Data type | Python syntax | Description |
| --- | --- | --- |
| Integer | int | Whole number Example, - 10 100 300 |
| Floating Point | float | Number with decimal points Example, - 11.50 100.02 |
| String | str | Ordered sequence of characters. Example, - "Hello" 'Hi' "200". Able to represent in single quote OR in double quote |
| List | list | Ordered sequence of Objects. Example, - [10, 'Hello', 20] |
| Dictionaries | dict | Unordered key-value paired. Example,- {"key1":"value1", "key2":"value2"} |
| Tuples | tup | Ordered immutable sequence of objects: {"hey", 200, "Hello"}. **Note:** Once tupple is create, we can't change its sequence at runtime. |
| Sets | set | Unordered collection of unique objects: {"A", "F", "G"} |
| Booleans | bool | logical value indicating true OR false |

### Few datatype with explaination & examples:
- [**string**](string/)
- [**list**](list/)

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)
