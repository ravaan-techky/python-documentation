##Python
### Zip and Unzip files
 - we can able to fo zipping and unzipping for files OR folder with the help of zipfile module.
 
 **Example to zipping files:**
 
 - First create file - file_one.txt in jupyter notebook
 
    ```python
    %%writefile file_one.txt
    Hello
    This is First File.
    End of File
    ```

 - Second file - file_two.txt using open function.
 
    ```python
    file_two = open('file_two.txt', 'w+')
    file_two.write('''
    Hello
    This is Second File.
    End of File
    ''')
    ```

  - Zipping above mentioned files with the help of zipfile module
  
    ```python
    import zipfile
    zipfile_object = zipfile.ZipFile('compression_file.zip', 'w')
    zipfile_object.write('file_one.txt', compress_type= zipfile.ZIP_DEFLATED)
    zipfile_object.write('file_two.txt', compress_type= zipfile.ZIP_DEFLATED)
    zipfile_object.close()
    ```
  
  - Unzipping above mentioned archive file with the help of zipfile module
  
    ```python
    import zipfile
    zipfile_object = zipfile.ZipFile('compression_file.zip', 'r')
    zipfile_object.extractall('extracted_contented')
    ```
    
    
 
