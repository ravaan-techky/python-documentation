## Python

### Math API module:
 - Math module provide all mathematical operation.
 - help(math) after importing math module you can use to see all math module functions.
 - numpi is module which has all advance math operation which most commonly use in AI ML projects.

**Example, -**
```python
num_var = 4.35
```

| Method | Description | Output |
| --- | --- | --- |
| math.floor(num_var) | returns the largest integer value that is less than or equal to a number. | 4 |
| math.ceil(num_var) |  returns the smallest integer value that is bigger than or equal to a number. |  5 |
| round(num_var) | rounding the number with the help of expotential number value |   4 |
| round(4.5) | round function always goes closer to event number in case of mid number of expotential value.  |  4 |
| round(4.7) | rounding the number with the help of expotential number value.  |  5 |
| round(5.5) | round function always goes closer to event number in case of mid number of expotential value.  |  6 |

**Example of few inbuilt keywords in math module, -**
```python
math.pi   # ==> PI value
math.e    # ==> Base of natural logarithms value
math.inf  # ==> A floating-point positive infinity.
math.nan  # ==> A floating-point “not a number” (NaN) value
```

### Random API module:
 - random module available in random package
 
**Example:**
```python
import random
random.randint(0, 100) # ==> generate random number which is in range of 0 to 100
```
**seed example:**
```python
import random
random.seed(100) # ==> seed used to generate same series of random integer.
random.randint(0, 100) # ==> generate random number which is in range of 0 to 100
```
Note: 
 - Above example when we run into Jupyter Notebook it should be in same row otherwise seed will not work on randint function
 - All time when we run above code it will always return same series of rundom integer

**random item from given list example:**
```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ,11, 12, 13, 14, 15]
random.choice(my_list) # ==> 5 (Random item will pick up from my_list here list is not affected)
```

**select multiple number with and without replacement from random series example:**
```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10 ,11, 12, 13, 14, 15]
# Sample with replacement. that means it allow duplicate item to be choosen
random.choices(population = my_list, k = 5) # ==> [2, 10, 14, 3, 2] (Random 5 items will pick up from my_list here list is not affected)
# Sample without replacement. that means duplicate item not allowed to be choosen
random.sample(population = my_list, k = 5) # ==> [2, 10, 14, 5, 15] (Random 5 items will pick up from my_list here list is not affected)
```

**random shuffle function example:**
```python 
my_list = [1, 2, 3, 4, 5, 6, 7]
random.shuffle(my_list) # shuffle the given list. shuffle function does not return anything.
print(my_list) # ==> [5, 3, 7, 1, 2, 6, 4]
```


**random uniform function example:**
```python 
import random
my_var = random.uniform(1, 10) #Random number is choose along with expotential value also
print(my_var) # ==> 5.609960188291158
```

**random gauss function **
Gaussian distribution. mu is the mean, and sigma is the standard deviation
```python 
import random
my_var = random.gauss(mu = 2, sigma = 1) #Random gauss function
print(my_var) # ==> 2.632637726905687
```

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)
