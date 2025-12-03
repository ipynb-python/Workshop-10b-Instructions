# Python Week 9 Assessed Workshop

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

# Workshop 9b

This workshop has three sections. 

The **average 2:1** student is expected to complete **most of parts 1 and 2** within the time allocated. 

It is expected that the only the **few fastest high 1st class** students in the class will complete **all of the tasks** in the time allocated.

The weighting for each section in the advanced workshops is approximately: part 1 (40%) part 2 (35%) part 3 (25%), but may be moderated to reflect difficulty of different workshops.

---

## Part 1

This section includes 10 short tasks covering skills on the module so far. 

If you get stuck on a particular task you are advised to move on and revisit it if you have time.

---

Markdown Source
#### Part `1a`

Work in file `part_1a.py`

The code below defines a list.

```python
mylist = [ "a", "b", "c" ]
```

**i.** Write code to add an entry `"d"` to the end of the list

**ii.** Print the length of `mylist`

---

#### Part `1b`

Work in file `part_1b.py`

The code below defines a dictionary.

```python
english = { 'start_msg': 'Hello' }
```

**i.** Write code that prints the dictionary entry for key: `start_msg`

**ii.** Write code to add the following entry to the dictionary:
* key: `"end_msg"`
* value: `"Bye"`

Check the entry was added using: `print(english)`

---

#### Part `1c`

Work in file `part_1c.py`

**i.** Define a function called `get_half` that takes a single argument: `num`. It should return a value which is half the number passed to the function.

**ii.** Add a line of code demonstrating how to use the function with the value `10`, storing the output from the function as variable: `result`.

Check the correct value (`5.0`) is returned using: `print(result)`

---

#### Part `1d`

Work in file `part_1d.py`

Use Python to find the average of values: `54.6`, `56.2`, `60.2` (e.g. add all values together and divide by `3`).

Store the result as: `av_time`

Check the correct value (`57.0`) is returned using: `print(av_time)`

---

#### Part `1e`

Work in file `part_1e.py`

The code below defines two variables with information about who was ruler of England in `1890`.

```python
year = 1890
ruler = "Victoria"
```

Use an f-string to print a message:

`In the year _ the ruler of England was _.`

Where the blanks `_` are filled using the relevant values in the variables.

---

#### Part `1f`

Work in file `part_1f.py`

The code below defines:
* A list of names stored as variable: `people`
* The name of an individual stored as variable: `person`

```python
people = [ 'Anne', 'Bea', 'Colin', 'Dan' ]
person = 'Anne'
```

The coder needs to check if name: `person` is included in this list: `people`.

Write an `if` statement to do this. Print `IN LIST` or `NOT IN LIST` according to the result.

---

#### Part `2a`

Work in file `part_2a.py`

```python
from pathlib import Path
```

Using the `pathlib` module write the following message into file: `message.txt`

`I am a text file`

---

#### Part `2b`

Work in file `part_2b.py`

```python
from pathlib import Path
```

File: `num_list.txt` contains numbers in word form (e.g. `two`, `seven`) each on a separate line.

Read in the contents of the file and use it to put each word into a Python list variable: `numbers`.

Check your work using: `print(numbers)`

---

#### Part `2c`

Work in file `part_2c.py`

```python
from pathlib import Path
```

Write code to find all files in the current directory with a `*.log` extension.

Loop over these files, extract the name, and print each one to screen.

Expected output (may be in different order):

```text
access_26_11_25.log
access_25_11_25.log
access_23_11_25.log
access_24_11_25.log
```

---

#### Part `2d`

Work in file `part_2d.py`

The code below defines variables storing weather data for the month of October.

```python
from pathlib import Path

date_str = "oct25"
temp = 8.2
rainfall = 65
```

Write some code that can save the info in these variables into a `.txt` file.

The code should name the file using the content of: `date_str` (i.e. in this case the file will save as: `oct25.txt`).

Your code should write these on two lines using the following format:

```text
Temperature (C): _
Rainfall (mm): _
```

Where the blank `_` are replaced with the appropriate value.

---

#### Part `2e`

Work in file `part_2e.py`

```python
from pathlib import Path
```

**i.** Write code to read in the content from file: `book.txt` and store this as variable: `book_str`.

**ii.** Find the number of characters in the loaded content and store as variable: `nchar`.

**iii.** Split `book_str` into a list of the words it contains and store as list variable: `words`.

**iv.** Find the number of words in the loaded content and store as variable: `nwords`.

*Hint: To split into words replace each newline character to a space, and split on spaces.*

Check your work using: `print(nchar, nwords)` (Expected output: `7589` `1386`)

---

#### Part `3a`

Work in file `part_3a.py`

```python
from pathlib import Path
```

Load in the file: `book_cleaned.txt`. This stores the cleaned text from `book.txt` with one word per line.

The cleaning process involves:
* all text was converted to lower case
* all non-letters (`a-z`) were removed

**i.** Print all words with a length more than `10` letters. You should display each word followed by its length (e.g. `disappeared` `11`).

**ii.** Count the number of times the word `pizza` appears in the book. Store this value in variable: `n_pizza` and print it.
*Hint: You can use the `.count()` method for counting matching entries in a list.*

**iii.** Use `set()` on the complete word list to find the set of unique words in the book. Store this as: `unique_words`.

**iv.** Make a dictionary: `word_counts`. Add entries to store the count of all words that appear `20` or more times in the book.

---

#### Part `3b`

Work in file `part_3b.py`

```python
from pathlib import Path
```

Write code that is able to load file: `book.txt`. It should clean the text as described above and save it to file: `mybook_cleaned.txt` (i.e. repeat the processing used to make `book_cleaned.txt`).

Hint. One option to elminate characters that are not letters is to use `.isalpha()` as demonstrated below:

```python
mystr = "abc 123 !?. xyz"
for letter in mystr:
     if letter.isalpha():
          print(letter)
```
    
---

### Submitting your work

Run the following lines in the terminal to stage, commit and push your code back to your GitHub repository:

```
git add .
git commit -m "completed 9b"
git push
```

To check your work has been saved you can run the line of code below in the terminal to get the web address of the repository in GitHub. Goto the repository and check the completed code files are stored.

```
git config --get remote.origin.url
```
