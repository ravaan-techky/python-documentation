## Python

### Decorators in pythons:

**Simple Example:**

- Defining Decorators
  ```python
  #Decorating result if divider is Zero.
  def decorate_dividation(func):
      def inner_dividation(num1, num2):
          if num2 == 0:
              print('num2 cannot be Zero!!!')
              return
          else:
              return num1 / num2
      return inner_dividation
  ```

 - Using decorator into function
  ```python
  @decorate_dividation
  def divide(num1, num2):
      print(num1 / num2)
  ```

  Input:
  ```python
  divide(10, 0)
  ```
  Output:
  ```python
  num2 cannot be Zero!!!
  ```

  Input:
  ```python
  divide(10,5)
  ```
  Output:
  ```python
  2.0
  ```
  
  
<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)