---
weight: 3
bookFlatSection: true
title: Python Cheat sheet
bookToc: true
---

Python Cheat sheet
=====

## Useful tricks
```py

# Terminate a Python script early.
    quit()
 
# For 1 statement on multiple lines, 
# use line continuation character (\).
# Good for blog post.
    def __str__(self):
        return "Name={}, Title={}, Hourly rate={}."\
                .format( self.name, self.title, self.__hourly_rate )
```

## String
```py
# Concatenation
    s1 = 'Open'
    s2 = 'Writings.net'
    print( s1+s2 ) # Output: OpenWritings.net
 
# Object to string: Use str() function
    import datetime
    now_str = "Today is " + str(datetime.datetime.now())
    print(now_str)
 
# Find and replace    
    string.replace(old_str, new_str, maxreplace) # maxreplace: Replace N occurrences matched.
 
# Replace using regular expression
    import re
    str="Example regex"
    test = re.sub(r"[Ee]", "a", str) # axampla ragax
 
# Join: string.join(iterable); iterable = list, string & tuple
    my_list = ['1', '3', '4', '5']
    separator = ','
    print( separator.join(my_list) ) # 1,3,4,5
```


## If statement

```py
# Conditions
    # Comparison operators
    # ==  : Values are equal.
    # !=  : Values are NOT equal.
    # <>  : Values are NOT equal.
    # >=  : Value is greater or equal.
    # <=  : Value is less or equal.
    # is  : Is the same object.
 
    if True and b > a:
        print("b is greater than a")
    elif a == b and b is not None:
        print("a and b are equal")
 
# Modulo
    if i%2==0:
        print('even')
    else:
        print('odd')
```

## List
```py

my_list=[]          # Empty list.
my_list=[1,2,3]     # Create a list with some values.
print( len(my_list) ) # Size of my_list.
 
my_list[2]      # Access the third element(Index starts at 0)
my_list[-1]     # Get last element.
 
my_list.append('a')         # Append a new value to my_list
my_list.insert(0, 'first')  # Insert 'first' at position 0
 
del my_list[1]      # Delete element at position 1.
my_list.remove('a') # Remove first element with value 'a'. 
 
# Loop through a list.
    for item in my_list:
        print(item)
 
# Loop through a list using range.
    for i in range(0, len(my_list)):
        print(my_list[i])
 
# Loop through a list and at the same time, get the index too.
    my_list = [1,3,5]
    for (i, item) in enumerate(my_list):
        print(i, item)
 
# Slicing
    first_two      = my_list[:2]    # Get the first two items.
    last_two       = my_list[-2:]   # Get the last two items.
    portion_of_list= my_list[2:4]   # Get items from position 2 to 4.
 
# For sorting, data type has to be the same. Can't mix int and string.
    my_list=[1,2,3]
    my_list.sort()              # Sort list permanently in alphabetical order.
    my_list.sort(reverse=True)  # Sort list permanently in reverse alphabetical order.
    my_list.reverse()           # Reverse the order of the list.   
```

## Loop
```py

# Loop through a list & get index at the same time.
    my_list = [1,3,5]
    for (i, item) in enumerate(my_list):
        print(i, item)
```

## Date & Time
```py

import datetime
 
today = datetime.date.today()
print(today)       # 2018-12-31
print("{}-{}-{}".format(today.year, today.month, today.day))
 
print(datetime.date(2011, 4, 13))  # 2011-04-13
print(datetime.date.fromtimestamp(1326244364)) # 2012-01-10
 
a_datetime = datetime.datetime(2011, 4, 13, 23, 33, 59)
print("{}-{}-{}".format(a_datetime.year, a_datetime.month, a_datetime.day))
print("{}:{}:{}".format(a_datetime.hour, a_datetime.minute, a_datetime.second))
print(a_datetime.timestamp())
 
# Convert date to string.
    now = datetime.datetime.now()
    print(now.strftime("%m/%d/%Y, %H:%M:%S")) # 04/04/2019, 12:45:08
 
# Convert string to date: string should match date representation.
#  All directives(%): https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior
    a_date = datetime.datetime.strptime("21 June, 2018", "%d %B, %Y")
    print(a_date) # 2018-06-21 00:00:00
    a_date = datetime.datetime.strptime("12/11/2018 09:15:32", "%d/%m/%Y %H:%M:%S")
    print(a_date) # 2018-11-12 09:15:32
 
# Add / Substract date
#  timedelta(days=0, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=0, weeks=0)
    today = datetime.datetime.now()
    days_ago_delta = datetime.timedelta(days = 5)
    days_ago_5 = today - days_ago_delta
    print(days_ago_5)
```

## Function
```py

def sum(a,b):
    return (a, b, a+b)
 
print( sum(3,4) ) # Output: (3, 4, 7)
```

ที่มาบทความ : https://openwritings.net/pg/python/python-cheat-sheet