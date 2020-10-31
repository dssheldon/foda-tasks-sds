# foda-tasks-sds
------

### Fundamentals of Data Analysis - Repo for Tasks 2020

------



#### Task for the week of October 5, 2020 - Writing a function 'counts'

##### What the function does

The objective of Task is to write a Python function called 'counts' that takes a list as input and returns a dictionary of unique items in the list as keys and the number of times each item appears as values.

##### How the function works

The function requires a list to be passed as an argument

It will then ask the user for input on whether the user wants to count upper and lower case items as unique. A message will appear on the screen:

```
Do you want the  count to be case sensitive:
Enter '1' to treat all as upper case
Enter '2' to treat all as lower case
Enter '3' to count in original case 
```

Depending on the choice the user makes, the function will treat the unique items in the list as case sensitive or otherwise (e.g. a list containing 'A' and 'a' will give a count of A:2 or a:2 in case option 1 or 2 are selected respectively; and A:1 , a:1 when option 3 is selected). If the user inputs anything else except 1,2 or 3 the program gives an error message and terminates

The function will return a dictionary of  unique items OR return an error message if the the  list has items which are outside the parameters (mentioned in the function scope and limitations below)

##### Function scope and limitations

The function accepts a list subject to the following limitations:\n",

- The list can contain any characters (alphanumeric, special characters etc.)
- The list can contain another list/tuples. However, that embedded list/tuples/dictionary cannot contain any further lists/tuples/dictionary. In other words ONLY one layer of embded lists or tuples or dictionaries is allowed
- The list can contain a dictionary. However, that dictionary cannot contain any further list, tuple or dictionary (see previous point). Furthermore, the embedded dictionary needs to contain only numeric values.
- The embedded lists, tuples and dictionaries will be added to the count of values in the main list

If the above limitations are exceeded the function will return and error and will terminate.
       
