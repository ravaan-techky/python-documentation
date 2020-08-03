## Python
String data type:

- Order sequence that can hold a variety of object types.
- list support indexing & splicing operation.
- list element can access through forward indexing or reverse indexing
- list can be nested and also have a variety of useful methods that can be called them to perform operation.
- list is mutuable. That means, - we can change element with the help of indexing.

Example, - 

```markdown
my_list = [1, 'Two', 23.0, 'Three']
```
![list_operations](../../images/list-operation.png)

**Indexing Operations:**

| Input | Output |
| --- | --- |
| my_list[0] | 'One' |
| my_list[5] | 'Six' |
| my_list[-2] | 'Five' | 

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

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
