![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document day 2

2024-06-03 Introduction to python for ODISSEI summer school students.

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: https://tinyurl.com/python-odissei-day2

Collaborative Document day 1: https://tinyurl.com/python-odissei-day1

Collaborative Document day 2: https://tinyurl.com/python-odissei-day2

[TOC]

##  🫱🏽‍🫲🏻 Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
## 🎓 Certificate of attendance

If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.
Please request your certificate within 8 months after the workshop, as we will delete all personal identifyable information after this period.

## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, raise your hand in zoom. Click on the icon labeled "Reactions" in the toolbar on the bottom center of your screen,
then click the button 'Raise Hand ✋'. For urgent questions, just unmute and speak up!

You can also ask questions or type 'I need help' in the chat window and helpers will try to help you.
Please note it is not necessary to monitor the chat - the helpers will make sure that relevant questions are addressed in a plenary way.
(By the way, off-topic questions will still be answered in the chat)


## 🖥 Workshop website

https://esciencecenter-digital-skills.github.io/2024-06-03-dc-socsci-python-odissei/

🛠 Setup

https://esciencecenter-digital-skills.github.io/2024-06-03-dc-socsci-python-odissei/#setup

## 📁 Download files
Download and unzip the data to the same location as your jupyter notebooks: https://tinyurl.com/python-odissei-data


## 👩‍🏫👩‍💻🎓 Instructors

Sven van der Burg, Sander van Rijn, Ewan Cahen

## 👩‍💻👩‍💼👨‍🔬🧑‍🔬🧑‍🚀🧙‍♂️🔧 Roll Call
Name/ pronouns (optional) / job, role / social media (twitter, github, ...) / background or interests (optional) / city

## 🗓️ Agenda
09:00	Welcome and icebreaker
09:15   Finish 'reusable code'
09:45	Reading data from a file using Pandas
10:15	Coffee break
10:30	Extracting row and columns and data aggregation using Pandas
11:30	Coffee break
11:45	Data visualization using Matplotlib
12:45	Wrap-up
13:00	END

## Welcome
- Feedback from yesterday
- Questions from yesterday

### 🥶 Icebreaker
If you could pick an animal you could be for a day: which animal would you pick?


## 🔧 Exercises

### Exercise: Creating functions
1. Write a function definition to calculate the volume of a cuboid. The function will use three parameters h, w and l and return the volume.
2. Supposing that in addition to the volume I also wanted to calculate the surface area and the total combined length of all of the edges. Would I (or should I) have three separate functions or could I write a single function to provide all three values together?
3. (Bonus) Use if/else statements to check whether the provided parameters are actually valid.
4. (Bonus) Compute the volume of cubes with edge 1, 2, 3, ... until 10. (Hint: Use the range() function and a for-loop)

#### Your answers

Use this as an example to make the code look nice:

```python
def example():
    print()
```



#### Solution:

```python
def get_cuboid_volume(h, w, l):
    '''
    Calculate volume based on height, width and length
    '''
    volume = h * w * l
    edges_length = 4*h + 4*w + 4*l
    return volume, edges_length
```

It is ususally best to keep your functions small and not return too many things

### Exercise: Reading in data using pandas

#### Pandas sep
1. What happens if you forget to specify `sep='\t'` when reading a tab delimited dataset?

#### Exercise: head and tail
1. As well as the `head()` method there is a `tail()` method. What do you think it does? Try it.
2. Both methods accept a single numeric parameter. What do you think it does? Try it.

#### (Bonus) Exercise: Print all columns
1. When we asked for the column names and their data types, the output was abridged, i.e. we didn’t get the values for all of the columns. Can you write a small piece of code which will print all of the values on separate lines. Paste your code in the collaborative document.
2. Using if statements, write a piece of code that prints 'big dataset' if the number of columns is larger than 10, and 'small dataset' if the number of columns is smaller.
3. Write a function that returns whether a dataset has more than 10 columns. (it should return a boolean value)

#### Your answers:

```python
def example():
    print()
```
 

#### Solutions

##### Pandas sep

1. If you forget the separator, a comma will be used as a seperator (which are not in this dataset)

##### head and tail

1. `head()` prints the first five rows, `tail()` the last five rows
2. If you give `head()` or `tail()` an integer argument, it will show that many rows instead

### Exercise: Pandas columns
What happens if you:
1. List the columns you want out of order from the way they appear in the file?
2. Put the same column name in twice?
3. Put in a non-existing column name? (a.k.a Typo)


#### Solution

1. They appear in the order you specified
2. It is shown twice
3. A `KeyError` is generated (look at the bottom of the error message)

### Exercise: Selecting rows and colums
1. Select all the rows for which `Q1` is equal to `Q2` or `numkid` is equal to 3, then select  the columns `daily1` and `daily2`.
2. (Optional) Take the first 10 rows of all the columns the header of which starts with `daily`.


#### Solution

Use the pipe symbol `|` (usually above your `Enter` key) for the`or` operation:

```python
df[(df.Q1 == df.Q2) | (df.numkid == 3)][['daily1', 'daily2']]
```

### Exercise: Number of values
Compare the count values returned for the `B_no_membrs` and the `E19_period_use` variables.
1. Why do you think they are different?
2. How does this affect the calculation of the mean values?
3. (optional): Use your search engine to find how to deal with missing values in pandas.

#### Solution

```python
df['B_no_membrs'].count()
```

```python
df['E19_period_use'].count()
```

```python
df[['B_no_membrs', 'E19_period_use']]
```

We see missing values, denoted by `NaN`. So `count()` doesn't count the `NaN` values.

The mean is still calculated:

```python
df[['B_no_membrs', 'E19_period_use']].mean()
```

What are the sums (`NaN` is skipped here):

```python
df[['B_no_membrs', 'E19_period_use']].sum()
```

```python
print(df['B_no_membrs'].sum() / df['B_no_membrs'].count())
print(df['E19_period_use'].sum() / df['E19_period_use'].count())
```

So the mean just skips the `NaN` values!

### Exercise: aggregation
In breakout rooms. Discuss the answers in your group and write the answers in the collaborative document.
1. Read in the SAFI_results.csv dataset.
2. Get a list of the different E26_affect_conflicts values.
3. Groupby E26_affect_conflicts and describe the results.
4. How many of the respondents never had any conflicts?
5. (optional) Using groupby find out whether farms that use water ('E01_water_use') have more plots ('D_plots_count') than farms that do not use water.

#### Your answers:

```python
def example():
    print()
```

- Group 1: 
    1. df = pd.read_csv('../data/data/SAFI_results.csv')
    2. df['E26_affect_conflicts'].unique()
    3. grouped_conflict = df.groupby(['E26_affect_conflicts'])
       grouped_conflict.describe()
    4. 46
    5. 

- Group 2: 
1. df = pd.read_csv('../data/SAFI_results.csv')
2. df['E26_affect_conflicts'].unique()
3. grouped_data = df.groupby('E26_affect_conflicts')
   grouped_data.describe()
4. 46
5. grouped_data = df.groupby(['E01_water_use','D_plots_count'])
   grouped_data.count()


- Group 3: 

2. df['E26_affect_conflicts'].unique()
3. grouped_data = df.groupby(['E26_affect_conflicts'])
    grouped_data.describe()
4. 46 respondents
5. grouped_data = df.groupby(['E01_water_use', 'D_plots_count'])
   grouped_data.describe()


- Group 4: 
```python
df['E26_affect_conflicts'].unique()
grouped_data = df.groupby['E26_affect_conflicts'])
grouped_date.describe()
46
grouped_data2=df.groupby[]

```
- Group 5: df['E26_affect_conflicts'].unique() | grouped_data = df.groupby('E26_affect_conflicts') grouped_data.describe() | 46 | yes 
- Group 6: 
```python
df = pd.read_csv('../data/SAFI_results.csv')
df['E26_affect_conflicts'].unique()
grouped_data = df.groupby(['E26_affect_conflicts'])
grouped_data.describe()
```
4. 46
5. Yes

#### Solutions

1. `df = pd.read_csv('../data/SAFI_results.csv')`
2. `df['E26_affect_conflicts'].unique()`
3. `df.groupby('E26_affect_conflicts').describe()`
4. `df.groupby('E26_affect_conflicts')['A01_interview_date'].count()` -> never: 46. Count will be the same for all columns, so we select (a random) one with `['A01_interview_date']` to limit the output
5. `df.groupby('E01_water_use')['D_plots_count'].mean()` -> no: 1.589744 < yes: 2.500000

### Exercise: (In breakout rooms) Plotting with Pandas

1. Make a histogram of the number of buildings in the compound (`buildings_in_compound`). Determine the appropriate number of bins, then include the `bins` argument in your function to improve the chart.
2. Make a scatter plot of `years_farm` vs `years_liv` and color the points by `buildings_in_compound`.
3. (Optional) Make a bar plot of the mean number of rooms per wall type (use columns `rooms` and `respondent_wall_type`). Hint: check out the function `plot.bar`, and recall how to use `groupby` to apply statistics to grouped data.

#### Your answers:

- Group 1: 
    1. df['buildings_in_compound'].hist(bins = 15)
    2. df.plot.scatter(x='years_farm',
                y='years_liv',
                c='buildings_in_compound',
               colormap= 'viridis')
- Group 2: 

1. df['buildings_in_compound'].hist(bins=15)
2. df.plot.scatter(x='years_farm',
                   y='years_liv',
                   c='buildings_in_compound',
                   colormap='viridis')

- Group 3: 
- Group 4: df['buildings_in_compound'].hist(bins=4)
- 
``` python
    1. 
```




- Group 5: df['buildings_in_compound'].hist(bins=15) | df.plot.scatter(x='years_farm',
                y='years_liv',
                c='buildings_in_compound', 
               colormap='viridis') | 
- Group 6: 
```python
df['buildings_in_compound'].hist(bins=8)
df.plot.scatter(x = 'years_farm',
                y = 'years_liv',
                c = 'buildings_in_compound',
               colormap = 'viridis')

```

#### Solutions:

1. `df.hist(column='buildings_in_compound', bins=8)`
2. `df.plot.scatter(x='years_farm', y='years_liv', c='buildings_in_compound', colormap='viridis')`

## 🧠 Collaborative Notes

### Functions

![structure of a Python function](https://datacarpentry.org/python-socialsci/fig/functionAnatomy.png)

If you forget a return statement in a function, this is not an error, because functions can also just do something. The return value will then automatically be `None`.

`None` is a special value that represents nothing.

If your variables are `None` when you didn't intend to, you might have forgotten a return statement in a function.

Writing good functions is hard. One reason is that naming a function is hard.

A good function does one thing well.

A good function is not too lang. A rule of thumb is to stick to 20 lines max, though sometimes you have to use more lines.

A short function allows you to easily keep in your head what it does.

Look at other people's code to see what good (and bad) code looks like.

If you have many functions, it might be a good idea to split them up in different files, where files that are related are in one file.

### Reading data from a file using Pandas

We will learn:

- What is Pandas?
- How do I read files using Pandas?

Pandas is a library for reading data in Python.

We have to import Pandas first:

```python
import pandas as pd
```

When reading a data file, it could help to print where we are currently:

```python
pwd
```

Read the data and assign it to a variable (`df` stands for dataframe):

```python
# You could also use an absolute path instead
df = pd.read_csv('./data/data/SN7577.tab', sep='\t')
```

**When typing the path of the data file, you can also start with a dot and a slash `./` (or two dots and a slash `../`) and hit the tab key; you can see all folders and files available and navigate through that.**

Check out the type of `df`:

```python
type(df)
```

Number of rows:

```python
len(df)
```

Number of rows and columns:

```python
df.shape
```

Display columns:

```python
df.columns
```

Types of the columns:

```python
df.dtypes
```

First 5 rows:

```python
df.head()
```

### Extracting row and columns

In a new notebook, import Pandas again:

```python
import pandas as pd
```

Import the data:

```python
# You could also use an absolute path instead
df = pd.read_csv('./data/data/SN7577.tab', sep='\t')
```

First 5 rows:

```python
df.head()
```

But this also shows we have 202(!) columns. We can use a subset of columns instead by specifying the indices:

```python
df = pd.read_csv('./data/data/SN7577.tab', sep='\t', usecols=[0, 1, 173, 174])
```

Now this will only show 4 columns:

```python
df.head()
```

We can also use columns labels instead:

```python
df = pd.read_csv('./data/data/SN7577.tab', sep='\t', usecols=['Q1', 'Q2', 'sex', 'age'])
df.head()
```

Show one column:

```python
df['Q1']
```

or, because the name is a valid Python variable name:

```python
df.Q1
```

Get multiple columns by passing a list inside square indexing brackets:

```python
df[['Q2', 'age']]
```

So `['Q2', 'age']` is a list, and the outer brackets are for selecting columns

Now we will work with **rows**

This displays the first 4 rows: (and skips the first row, because it has index 0) 

```python
df[1:5]
```

The **colon is necessary**; if you leave it out, it will look for a column with that name instead.

If we want to filter the rows that satisfies a condition, that looks like:

```python
df[(df.Q2 == -1)]
```

Only rows where the value of `Q2` is `-1` are included.

If you want to combine multiple criteria:

```python
df[(df.Q2 == -1) & (df.numage > 60)]
```

Filter rows *and* select only some columns:

```python
df[(df.Q2 == -1) & (df.numage > 60)][['Q1', 'Q2', 'age']]
```

Or do it in multiple steps:

```python
sub_df = df[(df.Q2 == -1) & (df.numage > 60)]
sub_df = sub_df[['Q1', 'Q2', 'age']]
sub_df
```

You have to include the `df` to make it work. Run the following to see what is does:

```python
df.Q2 == -1
```

It create a dataframe with two columns: one with the indices and one with boolean values (`True` or `False`) that shows the result of the filter.

We can also use *index location*. To get some rows:

```python
df.iloc[5:10]
```

Note that when using `loc`, the final index is included:

```python
df.loc[5:10]
```

Get rows and columns using `loc`:

```python
df.loc[5:10, ['Q1', 'Q2']]
```

With `iloc` only indices work, *not* column names:

```python
df.iloc[5:10, [0, 1]]
```

### Data Aggregation using Pandas

In a new notebook, import Pandas again:

```python
import pandas as pd
```

Read the data and assign it to a variable (`df` stands for dataframe):

```python
# You could also use an absolute path instead
df = pd.read_csv('./data/data/SAFI_results.csv')
```

Inspect the data:

```python
df.head()
```

Display some useful statistics about the data:

```python
df.describe()
```

Statistics for one column:

```python
df['B_no_membrs'].describe()
```

Count only:

```python
df['B_no_membrs'].count()
```

Mean only:

```python
df['B_no_membrs'].mean()
```

Print multiple values:

```python
print(df['B_no_membrs'].std())
print(df['B_no_membrs'].min())
print(df['B_no_membrs'].max())
print(df['B_no_membrs'].sum())
print(df['B_no_membrs'].mean())
```

**Categorical values**

This column in not numerical:

```python
df['C01_respondent_roof_type']
```

See the unique values:

```python
df['C01_respondent_roof_type'].unique()
```

There are only 3 values! Use grouping to see the statistics per unique value in the column:

```python
grouped_data = df.groupby('C01_respondent_roof_type')
grouped_data.describe()
```

For multiple columns:

```python
grouped_data = df.groupby(['C01_respondent_roof_type', 'C02_respondent_wall_type'])
grouped_data.describe()
```

That shows us a "group of groups", nicely formatted in a table.

To get the counts:

```python
grouped_data.count()
```

### Data visualisation using Matplotlib, Seaborn and Pandas

We will learn:

- create simple plots using pandas
- how to customise plots using matplotlob
- how to make super pretty plots with seaborn

Open an new notebook:

```python
import pandas as pd
df = pd.read_csv('./data/data/SAFI_full_shortname.csv')
```

To tell Jupyter that we want to show 

```python
%matplotlib inline
```

Make a first plot:

```python
df['years_liv'].hist(bins=20)
```

A more complicated plot where we group the data:

```python
df.hist(column='years_liv', by='village', layout=(1, 3), figsize=(12, 3), sharex=True, sharey=True)
```

Scatterplot:

```python
df.plot.scatter(x='gps_Latitude',
                y='gps_Longitude',
                c='gps_Altitude',
                colormap='viridis')
```

Boxplots:

```python
df.boxplot(by='village', column=['buildings_in_compound'])
```

We will now use Seaborn:

```python
import seaborn as sns
sns.boxplot(data=df, x='village', y='buildings_in_compound')
```

You can easily change the style:

```python
sns.set_style('dark')
```

```python
sns.lmplot(data=df, x='years_farm', y='years_liv', hue='village')
```

A more complicated example:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Generate some date for 2 sets of points.
x1 = pd.Series(np.random.rand(20) - 0.5)
y1 = pd.Series(np.random.rand(20) - 0.5)

x2 = pd.Series(np.random.rand(20) + 0.5)
y2 = pd.Series(np.random.rand(20) + 0.5)


# Add some features
plt.title('Scatter Plot')
plt.ylabel('Range of y values')
plt.xlabel('Range of x values')

# plot the points in a scatter plot
plt.scatter(x1, y1, c='red', label='Red Range')  # 'c' parameter is the colour and 'label' is the text for the legend
plt.scatter(x2, y2, c='blue', label='Blue Range')

plt.legend(loc=4)  # the locations 1,2,3 and 4 are top-right, top-left, bottom-left and bottom-right
# Show the graph with the two sets of points
plt.show()
```

**Next steps**

- learn about packages used in your field
- use Python in practice
- the internet is your friend (search engines, AI)
- get your code peer reviewed

## Wrapup
### 🚨🚨🚨 Fill in the post-workshop survey: 🚨🚨🚨
- [post-workshop survey link](https://www.surveymonkey.com/r/K7FXWVB)


## 📚 Resources

- [Pandas official website](https://pandas.pydata.org/)
