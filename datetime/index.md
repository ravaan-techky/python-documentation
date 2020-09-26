## Python

### datetime api:
 - datetime api imported from datetime package
 
Time API example, -
```python
import datetime
my_time = datetime.time(2, 10, 30)

#my_time.hour ==> 2 Hour (Support 24 Hour)
#my_time.minute ==> 10 minutes
#my_time.second ==> 30 Second
#my_time.microsecond ==> 000000
```

For Current Date API example, -
```python
import datetime;
curent_date = datetime.date.today()
print(curent_date) # ===> 2020-09-26
current_date.day # ===> 26
current_date.month # ===> 09	
current_date.year # ===> 2020
```

For formated Date API example, -
Date API example, -
```python
import datetime;
curent_date = datetime.date.today()
current_date.ctime() # ===> 'Sat Sept 26, 00:00:00 2020'
```

Replace operation from datetime API example, -
```python
from datetime import datetime
my_datetime_var = datetime(2021, 10, 2, 14, 15, 45)
print(my_datetime_var) # ===> 2021-10-02 14:15:45
my_datetime_var = my_datetime_var.replace(year = 2020)
print(my_datetime_var) # ===> 2020-10-02 14:15:45
```

Date difference API example, -
```python
from datetime import date
date1 = date(2019, 9, 26)
date2 = date.today()
result = date2 - date1
type(result)         # ==> datetime.timedelta
result.days          # ==> 366
result.seconds       # ==> 0
result.total_seconds # ==> 31622400.0
```

Datetime difference API example, -
```python
from datetime import datetime
datetime1 = datetime(2019, 9, 26, 20, 34, 56)
datetime2 = datetime(2020, 9, 26, 10, 14, 26)
result = datetime2 - datetime1
type(result)         # ==> datetime.timedelta
result.days          # ==> 366
result.seconds       # ==> 49170
result.total_seconds # ==> 31585170.0
```

<br/><br/>
[<i class="fa fa-arrow-left"></i> **Back**](/python-documentation/)
