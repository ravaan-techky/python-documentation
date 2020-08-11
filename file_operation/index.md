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

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](../)
