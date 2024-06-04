![](https://i.imgur.com/iywjz8s.png)


# Collaborative Document day 1

2024-06-03 Introduction to python for ODISSEI summer school students.

Welcome to The Workshop Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

This is the Document for today: https://tinyurl.com/python-odissei-day1

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
09:15	Introduction to Python and Python basics
10:15	Coffee break
10:30	Python control structures
11:30	Coffee break
11:45	Creating reusable code
12:45	Wrap-up
13:00	END

## 🥶 Icebreaker
- How is the energy?
- Number of years programming experience?
- Are you a morning person?

## Expectation management
- Some statistics about you:
    - Some people are completely or relatively new to programming
        - You are today's winners, learning how to program for the first time is super exciting and empowering! Your job is to ask as many questions as possible! Don't let others intimidate you 💪
    - Some people already know some Python
        - Have a look at the lesson material: https://datacarpentry.org/python-socialsci (NB: we only cover a subset). You can self-check if the level of this course is relevant for you! Even though this course is obligatory for the summer school, you are free to leave if you are not learning.
    - Most people are competent R practicioners but new to Python
        - Some things might be basic for you, especially in the beginning. But it is good to properly learn the basics. It will get more interesting towards the end (writing good functions, data analysis, plotting).


## 🔧 Exercises

### Exercise: Arithmetic and printing
Create a new cell and paste the following code into it:
```python=
print("a =", a, "and b =", b)
print(a + 2*b)
print(a + (2*b))
print((a + b)*2)
```
1. Remove all of the calls to the print function so you only have the expressions that were to be printed and run the code. What is returned?
2. Now remove all but the first line (with the 4 items in it) and run the cell again. How does this output differ from when we used the print function?

Bonus if you are done early:
* Practice assigning values to variables using as many different operators as you can think of. (see [this list of arithmetic operators](https://www.w3schools.com/python/gloss_python_arithmetic_operators.asp))
* Create some expressions to be evaluated using parentheses to enforce the order of mathematical operations that you require


Answers:
1. 10.283999999999999
2. `('a = 2", 2, 'and b =', 3.142)`: it prints the strings and variable values as a 'tuple', i.e., contained in ()'s
bonus:
```python
1 + 2 - 3 * 4 / 5 % 6 ** 7 // 8
```
> 3.0



### Exercise: string operations
Create a variable called `slugs` and assign it the string: 'The slug eats my young plants'
1. Use the `.find()` method to find the index of the word 'slug'.
2. Use string indexing to return only the word 'slug'.
3. (Bonus) Use the `.replace()` method to replace 'eats' with 'feasts on'
4. (Bonus) Make the lower case letters upper case and the upper case letters lower case. (Hint: there exists a method for this that we have not discussed, can you find it, for example using the internet?)
5. (Bonus) Try out the `.zfill()` method, what does it do?

Answers:
1. 4
2. `slugs[4:8]`
3. `slugs.replace('eats', 'feasts on')`
4. `slugs.swapcase()`
5. `x.zfill(42)` makes the total length 42 by adding 0's in front: '0000000000000The slug eats my young plants'

### Exercise: Lists and ranges
#### 1: List indexing
1. Create a cell with the code below.
```python=
num_list = [4,5,6,11]
```
2. Select the 1st element from this list. (Your code should return `4`)
3. Select the last element from this list. (Your code should return `11`)
4. Make a new list with the second and fourth element in this list. (Your code should return `[5,11]`)
5. (Bonus): Use the 'insert()' method to insert `5.5` in between `5` and `6`.
6. (Bonus): Which method removes an element at a specified position?
7. (Bonus): Sort the list in descending order.

**Answers:**

2. num_list[0]
3. num_list[3]  # or num_list[-1]
4. new_list = [num_list[1], num_list[3]]
5. num_list.insert(2, 5.5)
6. num_list.pop(position)
7. num_list.sort(reverse=True)

#### 2: Ranges
1. Create a list with `range()`:
```python=
list(range(3,12,2))
```
2. What happens if you change the step value (the third argument) to 1? And to 3? Or to -1? Did you expect this?
3. (Bonus) Create a list using the `range()` function, which contains the even numbers between 1 and 10 in reverse order: `[10,8,6,4,2]`.

**Answers:**

2. The following happens. Using -1 might be unexpected:
   - 1 -> shows every step: 3, 4, 5, ..., 11
   - 3 -> every 3rd: 3, 6, 9
   - -1 -> [] empty list: you cannot count backwards from 3 to 12

3. list(range(10, 0, -2))



### Exercise: if-statements

1. Start with the following code:
```python=
apple_cost = 0.5
bread_cost = 2.5
money = 2
```
2. Write an `if`-statement, replacing the ____ in the code below, that checks whether you can buy a bread with your money:
```python=
if _________
    print("I can buy bread!")
```

3. Add an `elif` to your statement, where you check if you can buy an apple instead.
```python=
elif _________
    print("At least I can buy an apple!")
```

4. Bonus: write a final `else` for the tragic scenario where you can buy neither bread nor apple.

Answer:
```python
if money >= bread_cost:
    print("I can buy bread!")
elif money >= apple_cost:
    print("At least I can buy an apple!"
else:
    print("Everyhing is too expensive :(")
```



### Exercise: for-loop
Suppose that we have a string containing a set of 4 different types of values separated by , like this:
```python=
variablelist = "01/01/2010,34.5,Yellow,True"
```
Research the `split()` method and write a for-loop that prints each of the 4 components of `variablelist`

**Answer:**
```python
for component in variablelist.split(','):  # or .split(sep=',')
    print(component)
```
> 01/01/2010
> 34.5
> Yellow
> True




## 🧠 Collaborative Notes

### Python Basics

```python
print('Hello world!')
```
<Press Shift+Enter to run the code in this cell>
> Hello world!


#### Some notebook shortcuts

There are two 'dimensions' in Jupyter Notebooks: inside a cell and on top of cells.
Pressing \<Enter> goes 'into' the cell, pressing \<ESC> exits the cell and switches on top of them.
Once on top of the cells, you can use the arrow keys to navigate to different cells, and you can use \<a> and \<b> to create new cells \<a>bove or \<b>elow the currently selected cell.

#### Variables
```python
a = 3
```
```python
a
```
> 3
```python
a = 2
b = 3.142
```
```python
a
```
> 2

:::warning
**Important**

Note that the value of variable `a` can be overwritten. This may get tricky if you execute cells in different orders! If you re-run the cell with `a = 3`, then `a` will be 3 again, even though reading from top to bottom, you might think it would be 2.

Two tips for that:
1. work from top to bottom as much as possible
2. look at the numbers in front of the cells to keep track of when a cell was last executed

You can still 'lose' code if you overwrite the content of the cell, or remove it entirely, because Python will remember what was run, even if the cell is gone.
:::


```python
type(a)
```
> int
```python
type(b)
```
>float
```python
s = "hello world"
type(s)
```
> str
```python
'Hello, this is Sven's name'
```
> SyntaxError: unterminated string literal (detected at line 1)

```python
"Hello this is Sven's name"
```
>Hello this is Sven's name

```python
'This is "a quote"'
```
This is "a quote"

#### Arithmetic operations

```python
a + b
```
> 5.14299999999995
```python
a * b
```
> 6.284
```python
c = a + b
```
```python
print(c)
```
> 5.14299999999995
```python
a + 2*b
```
> 8.283999999999999
```python
(a + b) * 2
```
> 10.283999999999999

#### Using

```python
print(a)  # use parenthesis for functions, inside them are arguments for the function
```
> 2
```python
print(a, b)
```
> 2 3.142
```python
print(a, b, sep='cool separator')
```
> 2cool separator3.142cool separatorwhatever

If you want help, you can press \<Shift + Tab> after `print`, or you can type
```python
help(print)
```
> Help on built-in function print in module builtins:
> 
> print(*args, sep=' ', end='\n', file=None, flush=False)
>     Prints the values to a stream, or to sys.stdout by default.
> 
>     sep
>       string inserted between values, default a space.
>     end
>       string appended after the last value, default a newline.
>     file
>       a file-like object (stream); defaults to the current sys.stdout.
>     flush
>       whether to forcibly flush the stream.

#### A bit more on data types

We can change the type of a variable:
```python
type(a)
```
> int
```python
a = float(a)
type(a)
```
> float

This sometimes loses information!
```python
a = 3.142
a = int(a)
type(a)
```
> int
```python
a
```
> 3

Not all type conversions work:
```python
s = 'hello world'
s = int(s)
```
> ---------------------------------------------------------------------------
> ValueError                                Traceback (most recent call last)
> Cell In[8], line 2
>       1 s = 'hello world'
> ----> 2 s = int(s)
> 
> ValueError: invalid literal for int() with base 10: 'hello world'

#### Strings

```python
name = "Sven"
```

Strings can be 'added', i.e., concatenated with `+`
```python
'Hello' + name + ', how are you?'
```
> 'Hello Sven, how are you?'

 `len()` gives the length of a string
```python
s = 'hello world'
len(s)
```
> 11

Every string is an object, and we can ask it questions using 'methods', i.e., functions associated to objects. Some methods include `startswith()` and `find`, which we call as follows:
```python
my_string = 'The quick brown fox'
my_string.startswith("The")
```
> True
```python
my_string.startswith("brown")
```
> False
```python
my_string.find("brown")
```
> 10

Since a string is an array of characters, we can address specific characters by indexing using square brackets `[]`, starting at 0:
```python
my_string[0]
```
> 'T'
```python
my_string[2]
```
> 'e'

We can also index multiple characters by specifying `start:end`, where `start` is inclusive, and `end` is exclusive, so `[0:3]` means from index 0 until but not including index 3.
```python
my_string[0:3]
```
> 'The'

If either `start` or `end` is omitted, will simply use the very start or end respectively
```python
my_string[3:]
```
> ' quick brown fox'
 

#### Booleans
Another data type is the logical 'boolean' which can be `True` or `False`. It is returned 

```python
answer = True
wrong_answer = False
type(answer)
```
> bool
```python
'hello' == 'hello'
```
> True
```python
'hello' == 'Hello'
```
> False
```python
3 != 77  # != -> is not equal
```
> True
```python
1 < 2
```
> True


#### The `list`
Lists can contain anything
```python
list1 = [6, 54, 89.3, name, True]
print(list1)
```
> [6, 54, 89.3, 'Sven', True]
```python
list1[1]
```
> 54

`range()` is a function to create a sequence of numbers
```python
list(range(5))
```
> [0, 1, 2, 3, 4]
```python
list(range(2, 11, 2))
```
> [2, 4, 6, 8, 10]


### Control Structures

#### if

When you only want code to be executed when some condition is met, you can use the `if`-statement to create a conditional code block. To tell Python what code is in the conditional block, we indent it with 4 spaces. When we are done with the block, we simply un-indent again.

In general that looks like this:
```python
if expression:
    statement 1
    statement 2
    ...
    statement n
    
statement always executed
```

Here's a specific example with actual comparisons and (un)indented code:
```python
value = 5
threshold = 4
print('Example 1\n')  # '\n' prints another line

print('value is', value, 'threshold is', threshold)
if value > threshold:
    print(value, 'is bigger than', threshold)

print('\nExample 2\n')
    
high_threshold = 6
print('value is', value, 'new threshold is', high_threshold)
if value > high_threshold:
    print(value, 'is bigger than', high_threshold)

print('\nExample 3\n')

mid_threshold = 5
print('value is', value, 'final threshold is', mid_threshold)
if value == mid_threshold:
    print(value, 'is equal to', mid_threshold)
```
> Example 1
> 
> value is 5 threshold is 4
> 5 is bigger than 4
> 
> Example 2
> 
> value is 5 new threshold is 6
> 
> Example 3
> 
> value is 5 final threshold is 5
> value 5 and threshold 5 are equal

Since `value > high_threshold` was `False`, we have to add something if we still want to print something for this example. We could add an explicit new `if`:
```python
if value <= high_threshold:
```
but that will be always checked regardless of the previous outcome. We can automatically skip it using `elif` instead. As a final case without further checks, we can add `else`:

```python
a = 3
b = 4
print('a =', a, 'b =', b)

if a > b:
    print('greater than')
elif a == b:
    print('equal')
else:
    print('smaller than')
```
> a = 3 b = 4
> smaller than

Try changing the value for `a` to 4 or 5, to see `equal` or `greater than` be printed.

#### while

A `while`-loop can be used to repeat the same code multiple times, `while` a certain condition is `True`

```python
# sum numbers from 1 to 10
n = 10
cur_sum = 0
i = 1
while i <= n:
    cur_sum += i  # `cur_sum += ...` is the same as `cur_sum = cur_sum + ...`
    i += 1

print("The sum from 1 to", n, "is", cur_sum)
```
> The sum from 1 to 10 is 55

#### for

The `for`-loop is also meant to run the same code multiple times, but here you know in advance how many iterations you want to do. For example, doing something for each entry in a list, since you know how long the list is.

```python
for i in [1, 2, 3]:
    print(i)
```
> 1
> 2
> 3

:::info
**Prefer `for` over `while`**

A for-loop is typically easier and less error-prone than a while-loop. If you can, always use a for-loop instead of a while-loop!

The equivalent while-loop would have been:
```python
numbers = [1, 2, 3]
cur_index = 0
while cur_index < len(numbers):
    i = numbers[cur_index]
    print(i)
    cur_index += 1
```
:::


```python
for name in ["Tom", 42, 3.142]:
    print(name)
```
> Tom
> 42
> 3.142

```python
for i in range(3):
    print(i)
```
> 0
> 1
> 2

```python
for i in range(2, 11, 2):
    print(i)
```
> 2
> 4
> 6
> 8
> 10

```python
for letter in "ABCDE":
    print(letter)
```
> A
> B
> C
> D
> E

```python
long_string = "The quick brown fox jumped over the lazy sleeping dog"
for word in long_string.split():
    print(word)
```
> The
> quick
> brown
> fox
> jumped
> over
> the
> lazy
> sleeping
> dog

### Reusable code
So far we discussed built-in functions, but it would be nice to be able to write our own functions!

```python
def get_item_count(items_str, sep):
    """
    This function takes a string with a list of items and a separator 
    and returns the number of items    
    """
    items_list = items_str.split(sep)
    num_items = len(items_list)
    return num_items
```

Everything that is needed for a good function definition:
![](https://codimd.carpentries.org/uploads/upload_5c7a8b5fb2b31d0b130b1b0b7f5447b9.png)

Get help on your own function:
```python
help(get_item_count)
```

Call our own `get_item_count` function:
```python
items_owned = "bicycle;television;solar_panel;table"
get_item_count(items_owned, ';')
num_items
```

The variable `items_list` is only defined inside the 'scope' of the function definition
```python
print(items_list)
```
```
name 'items_list' is undefined
```

We can add a default argument for the `sep` argument:
```python
def get_item_count(items_str, sep=';'):
    """
    This function takes a string with a list of items and a separator 
    and returns the number of items    
    """
    items_list = items_str.split(sep)
    num_items = len(items_list)
    return num_items
```

Calling the function without specifying the `sep` argument now also works:
```python
get_item_count(items_owned)
```

If you do not specify keyword arguments Python assumes you call the function with positional arguments:
```python
print(get_item_count(';', items_owned))
```
```
1
```


### Questions

**Q: What is the difference between Python and R for statistics and data processing?**
A: R is very purpose-built for statistics, Python is more versatile

**Q: I've heard Anaconda is no longer being used by professional programmers. Why do you still use it?**
A: For context, Anaconda is a package/environment manager that is available on all platforms Windows/Linux/Mac. There are a few reasons we use it:
- Out of the box, it comes with a lot of common dependencies for scientific programming pre-installed
- It is often the recommended way to install scientific packages made by other people
- Especially on Windows, it is still one of the easiest and most complete ways to get a working, stable Python installation

**Q: When should I use `elif`s instead of multiple `if`s?**
A: An `elif` is skipped if any `(el)if` in the same 'block' are matched. So `elif`s are best if only exactly 1 out of all checks has to be done, while separate `if`s are best if they are independent of each other and multiple may be `True`

## Wrap-up
### What did we do?
- Python basics: jupyter lab/notebooks, variables, data types, arithmetic, getting help, lists
- Control structures: if/else, while/for -loops
- Reusable code: write our own functions 

I hope you can appreciate that:
- Relearning the basics makes you a better programmer
- Python is indeed relatively easy to learn
- (if you are new to programming): Programming is superpowerful. And if you are not convinced yet: with these basics we are going to perform more and more complex actions tomorrow!

### What is actually our place in the summer school?
We teach the introduction to machine learning 'course' on day 2 and 3 of the summer school. 2 colleagues will serve as mentors in the second week CBS assignment.

### Homework: setup for machine learning during summer school
Follow the setup instructions here: https://github.com/INRIA/scikit-learn-mooc/blob/main/local-install-instructions.md Note that you already installed `conda`! We can help you out tomorrow if you face any issues.

### Tomorrow:
Same zoom link, chit-chat & questions from 8:45. Start 9:00 sharp.

### Feedback
Please give us feedback about today! 
Can you mention one thing that went well and one thing that can be improved?
Think of: pace, instructors, content, setup instructions, interaction, communication,
exercises, balance between live coding, slides, exercises etc.

#### 👍 What went well:
- The pace was perfect for me as a beginner
- Good pace, helpful exercises
- Good pace for beginners and good excercises and explanations. Very slow pace for people with programming experience. But it is difficult to get choose the right pace for a mixed group.
- Good pace, I'm a beginner and everything was clear
- Good pace, the calm manner instruction, the nice interchange of live-coding and (simple) exercises. Appreciate occasional checks for appropriate pace & the breaks :)
- The pace was good and it was nice to first learn about something and then have an exercise about it.

#### 🤔 What can be improved:
- For me , online courses are relatively tough, so maybe the ratio lecture:exercises can be a bit heavier on the exercises 
- In general, hard to think of any. If i must: Perhaps you can think of a way to keep track of who is fully following along, and those that are just listening (because they for instance already know the material or have a difficult set-up), so that your list of names to check for exercises is up-to-date
- Perhaps we will do this tomorrow, but it would be nice to apply the things we have learned to social science data to see how we can use the code in practice when doing social science research.
-
-
-

#### Sven's summary:
- We will have more and longer exercises today as the matter becomes more complex and interesting
- Indeed we will try to keep the list of names under exerices more up-to-date
- We will use a social science dataset today


## 📚 Resources

* Non-integer numbers on computers are called [floating point numbers](https://docs.python.org/3/tutorial/floatingpoint.html), that may behave differently than you may expect
