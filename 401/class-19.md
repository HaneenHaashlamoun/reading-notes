# Automation

# Python Regular Expression Tutorial
Discover the power of regular expressions with this tutorial. You will work with the re library, deal with pattern matching, learn about greedy and non-greedy matching, and much more!

![Regex](https://files.realpython.com/media/Regular-Expressions-Regexes-in-Python-Part-1_Watermarked_1.ffa77de784ec.jpg)

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.

This tutorial will walk you through the important concepts of regular expressions with Python. You will start with importing re - Python library that supports regular expressions. Then you will see how basic/ordinary characters are used for performing matches, followed by wild or special characters. Next, you'll learn about using repetitions in your regular expressions. You'll also learn how to create groups and named groups within your search for ease of access to matches. Next, you'll get familiar with the concept of greedy vs. non-greedy matching.

This already seems like a lot, and hence, there is a handy summary table included to help you remember what you've seen so far with short definitions. Do check it out!

This tutorial also covers some very useful functions provided by the re library, such as: compile(), search(), findall(), sub() for search and replace, split(), and some more. You will also learn about compilation flags that you can use to make your regex better.

In the end, there is a case study - where you can put your knowledge in use! So let's regex...

# Regular Expressions in Python

In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:

``` 
import re
```

The re library in Python provides several functions that make it a skill worth mastering. You will see some of them closely in this tutorial.

## Basic Patterns: Ordinary Characters
![Characters](https://i0.wp.com/www.novixys.com/blog/wp-content/uploads/2018/02/regex.png?fit=700%2C400&ssl=1)
You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

Examples are 'A', 'a', 'X', '5'.

Ordinary characters can be used to perform simple exact matches:

```
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
```

```Match!```

Most alphabets and characters will match themselves, as you saw in the example.

The match() function returns a match object if the text matches the pattern. Otherwise, it returns None. The re module also contains several other functions, and you will learn some of them later on in the tutorial.

For now, let's focus on ordinary characters!

Do you notice the r at the start of the pattern Cookie?

This is called a raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.

For example, \ is just a backslash when prefixed with an r rather than being interpreted as an escape sequence. You will see what this means with special characters. Sometimes, the syntax involves backslash-escaped characters, and to prevent these characters from being interpreted as escape sequences; you use the raw r prefix.

TIP: You don't actually need it for this example; however, it is a good practice to use it for consistency.

## Wild Card Characters: Special Characters

Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

Let's check out some examples to see the special characters in action...
![WildCard](https://blog.finxter.com/wp-content/uploads/2020/10/regex_asterisk-1024x576.jpg)

But before you do, the examples below make use of two functions namely: search() and group().
With the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.
The group function returns the string matched by the re. 

. - A period. Matches any single character except the newline character.

```re.search(r'Co.k.e', 'Cookie').group()```

```'Cookie'```

^ - A caret. Matches the start of the string.

This is helpful if you want to make sure a document/sentence starts with certain characters.

```
re.search(r'^Eat', "Eat cake!").group()

## However, the code below will not give the same result. Try it for yourself:
# re.search(r'^eat', "Let's eat cake!").group()
```
```'Eat'```

$ - Matches the end of string.

This is helpful if you want to make sure a document/sentence ends with certain characters.

```
re.search(r'cake$', "Cake! Let's eat cake").group()

## The next search will return the NONE value, try it:
# re.search(r'cake$', "Let's get some cake on our way home!").group()
```

```'cake'```

[abc] - Matches a or b or c.

[a-zA-Z0-9] - Matches any letter from (a to z) or (A to Z) or (0 to 9).


\ - Backslash.
Perhaps, the most diverse metacharacter!!

* If the character following the backslash is a recognized escape character, then the special meaning of the term is taken.
* Else if the character following the \ is not a recognized escape character, then the \ is treated like any other character and passed through.

* \ can be used in front of all the metacharacters to remove their special meaning.


There is a predefined set of special sequences that begin with '\' and are also very helpful when performing search and match. Let's look at some of them up close...

\w - Lowercase 'w'. Matches any single letter, digit, or underscore.

\W - Uppercase 'W'. Matches any character not part of \w (lowercase w).


\s - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.

\S - Uppercase 'S'. Matches any character not part of \s (lowercase s).

\d - Lowercase d. Matches decimal digit 0-9.

\D - Uppercase d. Matches any character that is not a decimal digit.

The + symbol used after the \d in the example above is used for repetition. You will see this in some more detail in the repetition section later on...

\t - Lowercase t. Matches tab.

\n - Lowercase n. Matches newline.

\r - Lowercase r. Matches return.

\A - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.

\Z - Uppercase z. Matches only at the end of the string.

\b - Lowercase b. Matches only the beginning or end of the word.

------------------------------------------------

# shutil — High-level File Operations
![shutil](https://techbit.in/wp-content/uploads/2021/06/File-Decluttering-Using-Python-360x240.jpg)

The shutil module includes high-level file operations such as copying and archiving.

### Copying File Metadata
By default when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file to another, use copymode().

### Working With Directory Trees
shutil includes three functions for working with directory trees. To copy a directory from one place to another, use copytree(). It recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.

### Finding Files
The which() function scans a search path looking for a named file. The typical use case is to find an executable program on the shell’s search path defined in the environment variable PATH

### Archives
Python’s standard library includes many modules for managing archive files such as tarfile and zipfile. There are also several higher-level functions for creating and extracting archives in shutil. get_archive_formats() returns a sequence of names and descriptions for formats supported on the current system.

### File System Space
It can be useful to examine the local file system to see how much space is available before performing a long running operation that may exhaust that space. disk_usage() returns a tuple with the total space, the amount currently being used, and the amount remaining free.

      
© Haneen Hashlamoun