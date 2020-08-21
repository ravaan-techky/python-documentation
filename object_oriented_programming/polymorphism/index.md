## Python
### Polymorphism in pythom

- Creating abstract base class as Addition
  ```python
  class Addition():
      def __init__(self):
          print('Addition Initialized...')
      
      def add(self, variable1, variable2):
          raise NotImplementedError('Subclass must implement this abstract method.')
  ```

- Calling abstract method from Addition class
  ```python
  addition = Addition()
  addition.add(12,13)
  ```
  Output =>
  ```python
  Addition Class Initialized...
  ---------------------------------------------------------------------------
  NotImplementedError                       Traceback (most recent call last)
  <ipython-input-7-5dac7ee9222c> in <module>
        1 addition = Addition()
  ----> 2 addition.add(12,13)
  
  <ipython-input-5-136ec17b261c> in add(self, variable1, variable2)
        4 
        5     def add(self, variable1, variable2):
  ----> 6         raise NotImplementedError('Subclass must implement this abstract method')
  
  NotImplementedError: Subclass must implement this abstract method
    ```

- Creating child class to implement abstract method
  ```python
  class NumberAddition(Addition):
      def __init__(self):
          print('Number Addition Initialized...')
          
      def add(self, num1, num2):
          if type(num1) != int or type(num2) != int:
              raise TypeError('Only Integer parameter allowed.')
          else:
              return num1 + num2
  ```
  
- Calling add method from NumberAddition class
  ```python
  numAddition = NumberAddition()
  numAddition.add(12, 12)
  ```
  Output =>
  ```python
  Addition Initialized...
  Number Addition Initialized...
  24
  ```
  
  ```python
  numAddition = NumberAddition()
  numAddition.add(12, 12.45)
  ```
  Output =>
  ```python
  ---------------------------------------------------------------------------
  TypeError                                 Traceback (most recent call last)
  <ipython-input-25-149ec91b7a27> in <module>
  ----> 1 numAddition.add(12, 12.4)
  
  <ipython-input-23-2245da1316ad> in add(self, num1, num2)
        5     def add(self, num1, num2):
        6         if type(num1) != int or type(num2) != int:
  ----> 7             raise TypeError('Only Integer parameter allowed.')
        8         else:
        9             return num1 + num2
  
  TypeError: Only Integer parameter allowed.
  ```
- Creating child class to implement abstract method
  ```python
  class StringAddition(Addition):
      def __init__(self):
          Addition.__init__(self)
          print('String Addition instance')
          
      def add(self, num1, num2):
          if type(num1) != str or type(num2) != str:
              raise TypeError('Only String parameter allowed.')
          elif not num1.isdigit() or not num2.isdigit(): 
              raise TypeError('Only digit allowed.')
          else:
              return int(num1) + int(num2)
  ```
  
- Calling add method from StringAddition class
  ```python
  stringAddition = StringAddition()
  stringAddition.add('12', '12')
  ```
  Output =>
  ```python
  Addition Initialized...
  Number Addition Initialized...
  24
  ```
  
  ### Creating polymorphism by adding new function:
  
  ```python
  def add(instanceType, param1, param2):
    if type(instanceType) == NumberAddition or type(instanceType) == StringAddition:
        return instanceType.add(param1, param2)
    else:
        raise NotImplementedError('Method with this parameter is not implemented.')
  ```
  
  ```python
    add(stringAddition, '12', '15')
  ```
  Output =>
  ```python
    27
  ```


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/object_oriented_programming)
