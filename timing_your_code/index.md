## Python
### Timing your Code
 - Simply tracking your elapsed
 - Using the timeit module
 - Special %%timeit magic for Jupyter Notebook
 - Timeit module used to calculate performance of functionality with available solutions.

### Simply tracking your elapsed
**Solution 1 implementation:**
   ```python
   def method_one(number):
      return [str(num) for num in range(number)]
   ```

 Calling one time:
 
   ```python
   import time
   #Current time before running code
   start_time = time.time()
   
   #run method
   method_one(100000)
   
   #Current time after running code
   end_time = time.time()
   
   #Calculate differences
   elapsed_time = end_time - start_time
   print(f'Elapsed Time = {elapsed_time}') # ==> Elapsed Time = 0.019519329071044922
   ```

**Solution 2 implementation:**
   ```python
   def method_two(number):
      return list(map(str, range(number)))
   ```

 Calling one time:
 
   ```python
   import time
   #Current time before running code
   start_time = time.time()
   
   #run method
   method_two(100000)
   
   #Current time after running code
   end_time = time.time()
   
   #Calculate differences
   elapsed_time = end_time - start_time
   print(f'Elapsed Time = {elapsed_time}') # ==> Elapsed Time = 0.2002100944519043
   ```

### Using the timeit module

**Solution 1 implementation:**
   ```python
   def method_one(number):
      return [str(num) for num in range(number)]
   ```

   Calling 1 time:
   ```python
   method_one(10) # ==> ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
   ```
   
   Calling multiple time:
   
   Input:
   ```python
   %%timeit
   method_one(100)
   ```
   
   Output:
   ``'python
   16.3 µs ± 99.5 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)
   ```

**Solution 2 implementation:**
   ```python
   def method_two(number):
       return list(map(str, range(number)))
   ```
  
   Calling 1 time:
   ```python
   method_two(10) # ==> ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
   ```
   
   Calling multiple time:
   
   Input:
   ```python
   %%timeit
   method_two(100)
   ```
   
   Output:
   ```python
   13.3 µs ± 263 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)
   ```
   
   
