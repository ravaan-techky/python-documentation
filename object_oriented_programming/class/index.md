## Python
Python Classes

### Object Oriented Programming

- Instance variable / attribute is need to decalre inside constructor and those are accessible in method with the help of self keyword.
- Instance level variable is accessibke outside of class with the help of instance variable.
- Class level variable / attribute is need to declare outside of constructor and those are accessible in method with the help of class name.
- Class level variable is also accessible outside of class with the help of class name. Class Level variable is global variable for all instances of class.

**Class creation syntax**

```python
# Class name and usage
class ClassName():

    # class level attribute
    classLevelAttribute = ''

    # Constructor declaration
    def __init__(self, param1, param2):
        #instance attribute param1 initialization
        self.param1 = param1
        #instance attribute param2 initialization
        self.param2 = param2
  
    #Method declaration
    def method(self):
        //some operation
        print(f'Instance Parameter 1  : {self.param1}')
        print(f'Class Level Parameter : {ClassName.classLevelAttribute}')
```

**Class creation example**

```python
#Class for Student Information
class StudentInfo():
    
    #Class level attribute is available for all isntance of class
    schoolName = 'SBP Internation School'
    
    #Constructor with argument
    #name - string
    #address - string
    #marks - list
    def __init__(self, name, address, marks):
        self.name = name
        self.address = address
        self.marks = marks
    
    #Display student information
    def showStudentInformation(self):
        print('######################################################')
        print(f'School  :{StudentClass.schoolName}')
        print(f'Name    :{self.name}')
        print(f'Address :{self.address}')
        print(f'Marks   :{self.marks}')
        print(f"Grade : {self.displayResult(['F','B','A','A+'])}")
        print('######################################################')
        
    #Calculate Percentage of Marks
    def calculatePercentage(self):
        return (sum(self.marks) / len(self.marks) * 150) * 100.00
    
    #Display Result
    def displayResult(self, grades):
        percentage = self.calculatePercentage()
        if percentage < 35.00:
            print('RESULT: FAIL')
            return grades[0]
        elif percentage < 60.00:
            print('RESULT: SECOND CLASS')
            return grades[1]
        elif percentage < 75.00:
            print('RESULT: FIRST CLASS')
            return grades[2]
        else:
            print('RESULT: DISTINCTION')
            return grades[3]
```

**Usage of class to create object**
```python
    studentInfo = StudentInfo('John Smith', 'Pune', [120, 130, 140])
    StudentInfo.showStudentInformation()
```


<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/object_oriented_programming)
