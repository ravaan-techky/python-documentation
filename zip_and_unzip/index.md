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

**zipfile module:**
  - Zipping above mentioned files
  
    ```python
    import zipfile
    zipfile_object = zipfile.ZipFile('compression_file.zip', 'w')
    zipfile_object.write('file_one.txt', compress_type= zipfile.ZIP_DEFLATED)
    zipfile_object.write('file_two.txt', compress_type= zipfile.ZIP_DEFLATED)
    zipfile_object.close()
    ```
  
  - Unzipping above mentioned archive file
  
    ```python
    import zipfile
    zipfile_object = zipfile.ZipFile('compression_file.zip', 'r')
    zipfile_object.extractall('extracted_contented')
    ```

**shutil module:**

 - shutil module also used to make and unpack archive. This uses folder as source while making archive while uses file while upacking archive as source
 
 - making archive from directory as source. second parameter in make_archive represent format of archive. It may - 'zip' or 'tar'
    ```python
    import os
    import shutil
    current_dir = os.getcwd()
    dir_to_zip = current_dir + '//extracted_contented'
    zip_file_name = 'directory_zip'
    shutil.make_archive(zip_file_name, 'zip', dir_to_zip);
    ```
    
   - upacking archive from file to destination directory. third parameter is format of archive. It may - 'zip' or 'tar'
   ```python
   import os
   import shutil
   current_dir = os.getcwd()
   zip_file_name = 'directory_zip.zip'
   zip_to_dir = current_dir + '//unpack_content'
   shutil.unpack_archive(zip_file_name, zip_to_dir, 'zip' )
   ```
 
