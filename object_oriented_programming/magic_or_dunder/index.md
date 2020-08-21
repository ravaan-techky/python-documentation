## Python

### Magic OR Dunder method in Python
 - These methods provide flexibility use python built-in function with custom object
 - Here is few magic methods, - 
 
 |Python Built-In Function| Class level method declaration | Description |
 | --- | --- | --- |
 | print{instance} | _ _str__(self) | This method return instance string representations. |
 | len{instance} | _ _len__(self) | This method return length attribute of instance. |
 | del instance| _ _del__(self) | This method delete instance from memory. |
 
 - Example. -
 
   ```python
   #class to store book information.
   class BookInformation():
       def __init__(self, bookName, bookAuthor, bookPages):
           self.bookName = bookName
           self.bookAuthor = bookAuthor
           self.bookPages = bookPages
           print('BookInformation instance created.')
   
       def __str__(self):
           return f'Name - {self.bookName} Author - {self.bookAuthor} Pages - {self.bookPages}'
       
       def __len__(self):
           return self.bookPages
       
       def __del__(self):
           print(f'Deleting book information of name - {self.bookName}')
   ```

   ```python
   #Creating an custom instance of BookInformation class
   book = BookInformation('Java Book','Bhushan Patil', 300)
   ```
   Output =>
   ```
   BookInformation instance created.
   ```

   ```python
   #Printing book instance
   print(book)
   ```
   Output =>
   ```
   Name - Java Book Author - Bhushan Patil Pages - 300
   ```

   ```python
   #Checking length of book.pages attribute.
   len(book)
   ```
   Output =>
   ```
   300
   ```

   ```python
   #Deleting book instance from memory.
   del book
   ```
   Output =>
   ```
   Deleting book information of name - Java Book
   ```


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/object_oriented_programming)
