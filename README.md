# Python Week 10 Assessed Workshop

#### Run the following code in the CodeSpaces terminal to download and setup the workshop files in your repository:

```
wget https://github.com/ipynb-python/Workshop-10b-Instructions/raw/refs/heads/main/workshop10.zip; unzip workshop10.zip
```

---

#### Note on workshop attendance...

For advanced workshops completion of the activities must be under invigilated conditions.

Please make sure you sign the workshop attendance sheet. 

Code should autosave, but you must still commit your work at the end of the workshop before leaving.

---

**Do all coding in CodeSpaces only** 

You may use the following cheat sheets if you need to look up any Python commands.

https://github.com/phil-lewis-exe/PythonCheatSheets

**This week you should not use any other websites to help you code.**

**You must ask if you need to use a website to translate the task questions**

**Mobile phones may not be used in class**

---

## TASKS

# Workshop 10b

This workshop has three sections. 

The **average 2:1** student is expected to complete **most of parts 1 and 2** within the time allocated. 

It is expected that the only the **few fastest high 1st class** students in the class will complete **all of the tasks** in the time allocated.

The weighting for each section in the advanced workshops is approximately: part 1 (40%) part 2 (35%) part 3 (25%), but may be moderated to reflect difficulty of different workshops.

---

## Part 1

This section includes short tasks covering skills on the module so far. 

If you get stuck on a particular task you are advised to move on and revisit it if you have time.

---

#### Part 1a

Look at the following example that defines variable `var1`
then displays info about the type of object `var1` is.

```python
var1 = "hello"
print("var1: str")
```

Edit the print lines below
so they display the right object types
for `var2` and `var3` following the format
from the example above.    


```python
var2 = 0.6
var3 = 4

print("var2: ")
print("var3: ")
```

Choose from:

`int` `float` `bool` `str` `list` `dict` `tuple`


---

#### Part 1b

Write code to do the calculation below and 
store the result as variable: `z`

your code should make use of the variable `x`
as defined below so it would work if a 
different value is used 

```
        6 + x
 z =   -------
        6 - x
```

Test your code with: `print(z)`

Start with the code line:

```python
x = 2
```

---

#### Part 1c

Create a tuple with name: `mytuple`
that stores the values: 12, 4, 5

Test your code using: `print(mytuple)`

---

#### Part 1d

The following code defines a list
storing a set of strings

```python
mylist = [ "I", "II", "III", "IIII", "V", "VI" ]
```

Create a variable named: `myslice`
that selects the first 3 items from `mylist`

Test your code using: `print(myslice)`

---

#### Part 1e

Write a function named: `double_print`
that takes a single argument: `msg`

The function should print this variable twice.

e.g. if we pass in the value `banana` the
output would be:

```
banana
banana
```

Add code to demonstrate the function
using argument: `hello`

---

#### Part 1f

The following code defines a list
storing a set of strings:

```python
mylist = [ "I", "II", "III", "IIII", "V", "VI" ]
```

Write code to loop over the list items and 
print out the number of `I`'s in each string.

It should display one value per line with expected output:

```
1
2
3
4
0
1
```

Hint. For a string `mystr` we could count the
number of `X`s it contains using:

```python
mystr.count("X")` 
```

---

#### Part 1g

The following dictionary has been set up to translate 
between digits 1-5 and simplified roman numerals:

```python
mydict = {
    1: "I",
    2: "2",
    3: "III",
    4: "IIII",
    5: "V",
}
```

The value for key `2` should be `II`.

Show how you can add an extra line of code to edit the relevant 
dictionary entry in `mydict` to update
this value.

Test your code with: `print(mydict)`

---

#### Part 1h

The following code can print a countdown
starting from an input argument `x`

```python
    def countdown(x):
       while x > 0:
           print(x)
           x = x - 1
   
    countdown(5)
```

Edit the code so:

i. the function takes a default argument: `10`

ii. the example shows how to call the function
to check the default argument works

-----

## Part 2

These tasks require you to write tests and handle exceptions.

---

#### Part 2a

The code below reads in a a username from
file: `user.txt`

```python
   from pathlib import Path
   
   filename = "user.txt"
   
   username = Path(filename).read_text()
   
   print(f"Hello {username}")
```

Edit the code to ensure that it can handle the situation
that file `user.txt` does not exist.

In this case an exception should not occur,
variable `username` should be set to: `nobody`
and the message below should be displayed:

```
File missing, using: nobody
```

followed by the result of the print statement which will be:

```
Hello nobody
```

----

#### Part 2b

The function `rn_to_digit` is supposed to take
a simplified roman numeral and translate it 
to its integer value.

Requirement: 
It should correctly translate the values below:

```
I II III IIII V VI VII VIII VIIII
1  2  3   4   5  6  7    8    9
```

e.g. `rn_to_digit("III")` should return the integer `3`

```python
   def rn_to_digit(num):
       total = 0
       total += num.count("I")
       total += num.count("V")
       return total
```

**i.** Work in file: `test_rn_to_digit.py` 

Write a test function that can be used by `pytest`
to check if the function works correctly for
the stated requirements.

Remember include the relevant import to load the
function to be tested from this file.


**ii.** Work in this file.
At the moment the function below includes an error. 

Edit the code to fix the function.


----

#### Part 2c

A coder wants to write a function to add 
two simplified roman numeral numbers that
will work for sums up to 100:

The basic pattern for the function is in place
as below

```python
def rn_add(a, b):
   total = 0
   # code to be added
   # ...
   return total
```

However before they write the function they decide 
write a test that can verify its behaviour.

Requirement:

It should work for any calculation that totals 100 or less.

e.g. `rn_add("I", "XX")` should return `21`

*YOU DO NOT HAVE TO WRITE THE FUNCTION CODE*

*YOU HAVE TO WRITE THE TESTS FOR THE FUNCTION*

Work in file: `test_rn_add.py`

Add test functions that can check if `rn_add`
works when given valid inputs (sum to 100 or less).

i.e. numerals involved could include:

```
I: 1:   V: 5,  X: 10,  D: 50, C: 100
```

Your test code does not have to test every possibility
but should check a suitable set of calculations

Remember include the relevant import to load the
function to be tested from this file

```python
def rn_add(a, b):
   total = 0

   return total
```

----

### Part 3

This task is more challenging and involves writing and testing a function.

---

#### 3a.

Work in file `part3.py`

Write a function: `rn_times_ten`

that takes input argument: `myval`

Requirement:

**Input argument:** roman numeral `str` in range 1-100

**Output:** a roman numeral `str` that is ten times bigger

Hint. You can do this by builing the output value
from the characters in the input string using rules:

```
I --> X   (i.e. 1 --> 10)
V --> D   (i.e. 5 --> 50)
X --> C   (i.e. 10 --> 100)
D --> L   (i.e. 50 --> 500)
C --> M   (i.e. 100 --> 1000)
```

i.e. 

`rn_times_ten("XIII")` should return `CXXX`

#### 3b.

Ensure the function includes code to
throw and exception if a user attempts to pass 
an input value with invalid characters


#### 3c. 

Add test code that is able to test your function
against the requirements.

Work in test file `test_rn_times_ten.py`

---

### Submitting your work

Run the following lines in the terminal to stage, commit and push your code back to your GitHub repository:

```
git add .
git commit -m "completed 10b"
git push
```

To check your work has been saved you can run the line of code below in the terminal to get the web address of the repository in GitHub. Goto the repository and check the completed code files are stored.

```
git config --get remote.origin.url
```
