## Python

### shutil & os module:
 - Open file
 - Edit file
 - Listing all files from folder.
 - Listing all files from nested child folders.
 - delete file / folder
 - rename file / move folder

**Important methods from os module:**

| methods | description |
| --- | --- |
| os.getcwd() | get current working directory |
| os.listdir() | list all files and folder from current working directory |
| os.listdir(dir_path) | list all files and folder from given directory path |
| os.walk() | iterate all files and nested child directories from current working directory. This return tuple object (folder, sub_folders, files) |
| os.walk(dir_path) | iterate all files and nested child directories from given directory. This return tuple object (folder, sub_folders, files) |
| os.unlink(path) | delete file / folder |

**Important methods from shutil module:**

| methods | description |
| --- | --- |
| shutil.copy(src_path, dest_path) | copy file from source path to destination path |
| shutil.copy2(src_path, dest_path) | copy file from source path to destination path along with all attribute from source file. Example, - executable permission, last change date, create by, created on, etc.  |
| shutil.move(src_path, dest_path) | move file from source path to destination path |
| shtuil.delete(path) | delete file / folder |
| shutil.rmtree(path) | delete file / folder. This operation will delete file / folder permenant from file system (Not use Recycle Bin). Most of developer not recommending this operation. |


**Example for os.walk method:**
```python
import os;
for folder, sub_folders, files in os.walk('D:\Workspaces\python-workspace\simple-code'):
	print(f'Folder {folder}')
	for sub_folder in sub_folders:
		print(f'\t\t Sub Folder - {sub_folder}')
	for file in files:
		print(f'\t\t File - {file}')
```
Output:
```python
Folder D:\Workspaces\python-workspace\simple-code
		 Sub Folder - .ipynb_checkpoints
		 File - Collections.ipynb
		 File - decorators.ipynb
		 File - generators.ipynb
		 File - Untitled.ipynb
Folder D:\Workspaces\python-workspace\simple-code\.ipynb_checkpoints
		 File - Collections-checkpoint.ipynb
		 File - decorators-checkpoint.ipynb
		 File - generators-checkpoint.ipynb
		 File - Untitled-checkpoint.ipynb
```

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)
