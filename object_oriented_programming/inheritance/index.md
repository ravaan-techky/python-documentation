## Python
Inheritance

### Inheritance in Python:

- Base class declaration
  ```python
  #Base Class Animal
  class Animal():
      #constructor
      def __init__(self):
          print('Animal Created')

      #Method - Who Am I ?
      def whoamI(self):
          print('I am animal')

      #Method - Eat method
      def eat(self):
          print('Animal is Eating')
  ```
  
 - Base class object creation
  ```python
  myAnimal = Animal()
  ```
 
  Output=>
  ```
  Animal Created
  ```
  
- Child class declaration
  ```python
  #Child Class Dog
  class Dog(Animal):
    #constructor
    def __init__(self):
        Animal.__init__(self)
        print('Dog Created')
  ```

- Child class object creation
  ```python
  myDog = Dog()
  ```
 
  Output=>
  ```
  Animal Created
  Dog Created
  ```

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/object_oriented_programming)
