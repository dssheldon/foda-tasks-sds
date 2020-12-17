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
       

#### Task for the week of November 2nd, 2020 - Writing a function 'dicerolls'

**What the function does**

This section of the workbook contains a function called 'dicerolls' that simulates the rolling of 'k' number of dice for 'n' number of rolls. 

**How the function works**

- The function requires two arguments to be passed to the function:
  - k: Which is the number of dice being rolled by the user
  - n: The number of times the user wants to roll 'n' number of dice
- The function accumulates the sum of the face values of each dice for each roll
- Once all rolls have been completed, the function returns a dictionary of each unique value rolled and the number of times that value was rolled.

**Function scope and limitations**

- The can only take positive integers as value for k and n.
- Any other value will be return an error message and terminate the function

**Analysis of running the function**

The workbook contains an analysis of running the function when 'k' dice are run 'n number of times' where k is 1, 2 , 3 and 4 respectively and n is 10,000 times for each change in k.

There are also individual and cumulative (superimposed) plots for each of the scenarios above and comments on the distribution/pattern that arises from running the above scenario



#### Task for the week of November 16th, 2020 - Distribution of a coin flip

**What the code does**

The section of the workbook contains code that simulates flipping a coin 100 times each for 1000 times. The code then plots the distribution of the output while comparing it to the normal distribution. 

**Running the code**

The code itself uses:

- binomial function within numpy to simulate 100 coin tosses, 1000 times, where each coin toss has 50% probability of landing on heads or tails
- plots the output of of the above, using the `distplot` function within seaborn.

**User input**

There is no user input for this code

**Analysis**

The workbook shows: 

1. the distribution of the standard binomial function within numpy and plots this distribution

2. the plot for the binomial distribution (as mentioned in the running the code section above)

3. a superimposed plot of the output from point 2 above and the 'normal distribution' plot 

The workbook analyses both distributions and concludes on the similarities and differences between the two plots.

The workbook also contains reference material showing the links between the binomial and the normal distributions.



#### Task for the week of November 30th, 2020 - Simpson’s paradox

**What the code does:**

In this section of the workbook contains that simulates data to demonstrate Simpson’s paradox. 

**Running the code:**

The code uses numpy to create four data sets, each with an x array and a corresponding y array. The code uses the numpy `linspace` function to generate four sets of data (x arrays) with sufficient data points to plot.

The code then uses the linear function `y = mx + c` to generate a a y array using a constant value for `m` but varying the values for `c`. The code then adds a normal distribution to the linear function in order to create `noise` within the y array.

The code the joins together all the x and y arrays respectively of four datasets into a 'cumulative' x and y arrays using the numpy `concatenate` function.

Each of the four datasets and the cumulative dataset is plotted using the seaborn regression plot function `regplot`

**Analysis of the Data and Demonstrating Simpson's **

The workbook then analyses the results of the plot:

- Each individual dataset shows a certain trend in contrast to the cumulative dataset which shows the opposite trend. Thus demonstrating Simpson's Paradox
- Analyses the R-Squared values for each of the datasets (including the cumulative dataset) and plots the R-squared values in a histogram
- Shows the impact of increasing the level of noise on the individual and collective datasets including the impact on the r-squared valued. Plotted the revised scatterplots and histograms using the revised data to show the contrast with the original data 