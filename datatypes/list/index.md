## Python
list data type:

- Order sequence that can hold a variety of object types.
- list support indexing & splicing operation.
- list element can access through forward indexing or reverse indexing
- list can be nested and also have a variety of useful methods that can be called them to perform operation.
- list is mutuable. That means, - we can change element with the help of indexing.

Example, - 

```markdown
my_list = [1, 'Two', 23.0, 'Three']
print(my_list)
Output => [1, 'Two', 23.0, 'Three']
```

### List operations

```markdown
my_list = ['One', 'Two', 'Three', 'Four', 'Five', 'Six']
```
![list_operations](../../images/list-operation.png)

**Indexing Operations:**

| Input | Output |
| --- | --- |
| my_list[0] | 'One' |
| my_list[5] | 'Six' |
| my_list[-2] | 'Five' | 

<br/>
**Slice Operations:**

| Input | Output |
| --- | --- |
| my_list[2:] | ['Three', 'Four', 'Five', 'Six'] |
| my_list[:3] | ['Once', 'Two', 'Three'] |
| my_list[2:5] | ['Three', 'Four'] |
| my_list[::] | ['One', 'Two', 'Three', 'Four', 'Five', 'Six'] |
| my_list[::2] | ['One', 'Three', 'Five'] |
| my_list[::3] | ['One', 'Four'] |
| my_list[::-1] | ['Six', 'Five', 'Four', 'Three', 'Two', 'One'] |

<br/>
**Other useful methods:**

| Method | Usage | Output | Additional Information |
| --- | --- | --- | --- |
| len() | len(my_list) | 6 | Method use to calculate length of given list |
| append | my_list.append('Seven') | ['One', 'Two', 'Three', 'Four', 'Five', 'Six', 'Seven'] | Method use append new element at the end of list |
| pop() | pop_element = my_list.pop() | Output: my_list = ['One', 'Two', 'Three', 'Four', 'Five', 'Six'] <br/> pop_element = 'Seven' | Method use to remove last element from the list. <br/> pop method also take index as parameter to remove element from specific location. <br/> we can use forward index or reverse index also. |
| sort() | my_list.sort() | sorted element list <br/> ['One', 'Two', 'Three', 'Four', 'Five', 'Six'] | Method use to sort given list. This method does not return anything. |
| reverse() | my_list.reverse() | reverse element list <br/> ['Six', 'Five', 'Four', 'Three', 'Two', 'One'] | Method use to reverse given list. This method does not return anything. |

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
