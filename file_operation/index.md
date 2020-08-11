## Python
File operations:

### File creation method in JUPYTER NOTEBOOK
Note: If we dont have Jupter notebook, we can use simple text editor to create file

```markdown
%%writefile sampleTest.txt
This is new file created.
This is second line of file.
This is third line of file.
```

### File operations:

| Method name | Syntax | Output | Additional Information |
| --- | --- | --- | --- |
| open | myFileObject = open('sampleTest.txt') | | Return file handle in myFileObject variable. |
| read | myFileObject.read() | This is new file created.\nThis is second line of file.\nThis is third line of file. | Once you call read() method on file object, it sets at the end of file. After that if we call it again in that case it will print empty string i.e., '' |
| seek | myFileObject.seek(0) | This method use to set file pointer to start of file.|
| close | myFileObject.close() |  | If file is open in Read / Write mode in that case need to close otherwise other cann't able to do any operation on file. |

### Example:

```python
# In jupyter notebook
%%writefile sampleTest.txt
This is new file created.
This is second line of file.
This is third line of file.

#File sampleTest.txt has been create in current directory.

#Creating file object
myFileObject = open('sampleTest.txt')

#Calling read method on file object
myFileObject.read()
#Output: This is new file created.\nThis is second line of file.\nThis is third line of file.

#Calling read method on file object. This time file cursor is at end of file location.
myFileObject.read()
#Output: ''

#Setting up file cursor to start of file location.
myFileObject.seek(0)

#Calling read method on file object
print(myFileObject.read())
#Output: This is new file created.
		 This is second line of file.
		 This is third line of file.
```

### IO Operation with key Example:
with keyword use for auto closing of file
```python
with open('sampleTest.txt') as myFileObject:
	print(myFileObject.read())
#Output: This is new file created.
		 This is second line of file.
		 This is third line of file.
```

### File Operation modes:

| Mode | Description |
| --- | --- |
| 'r' | Default set. Read only. |
| 'w' | Write only. (Will overwrite file OR create new file) |
| 'a' | Append only. (Will add content at end of file) |
| 'r+' | Reading and Writing |
| 'w+' | writing and Reading. (Overwrites existing file OR create a new file) |

```python
# In jupyter notebook
%%writefile sampleTest.txt
This is new file created.
This is second line of file.
This is third line of file.

#File sampleTest.txt has been create in current directory.
#Opening file into read mode.
with open('sampleTest.txt', mode = 'r') as fileObject:
	print(fileObject.read())
#Output: This is new file created.
		 This is second line of file.
		 This is third line of file.

#Opening file into append mode.
with open('sampleTest.txt', mode = 'a') as fileObject:
	fileObject.write('This is fourth line in file.')
#This will append content at the end of file.
#Note: If file is open in 'a' append mode then we can't call read method on it. It will give Unsupport method error.

#Opening file into append mode.
with open('sampleNewTest.txt', mode = 'w') as fileObject:
	fileObject.write('This is new file.')
#This will create new file. If file is already exist then it will be overwrite.
#Note: If file is open in 'w' write mode then we can't call read method on it. It will give Unsupport method error.
```

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
