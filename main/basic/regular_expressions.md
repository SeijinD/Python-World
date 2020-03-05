# Regular Expressions
---

RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.
RegEx can be used to check if a string contains the specified search pattern.

#### RegEx Module
Python has a built-in package called **re**, which can be used to work with Regular Expressions.
~~~~
import re 
~~~~

#### RegEx Functions
- ##### findall
  - Returns a list containing all matches
    ~~~~
    import re

    txt = "The rain in Spain"
    x = re.findall("ai", txt)
    print(x)
    ~~~~
- ##### search
  - Returns a Match object if there is a match anywhere in the string
    ~~~~
    import re

    txt = "The rain in Spain"
    x = re.search("Portugal", txt)
    print(x) 
    ~~~~
- ##### split
  - Returns a list where the string has been split at each match 
    ~~~~
    import re

    txt = "The rain in Spain"
    x = re.split("\s", txt)
    print(x) 
    ~~~~
- ##### sub
  - Replaces one or many matches with a string
    ~~~~
    import re

    txt = "The rain in Spain"
    x = re.sub("\s", "9", txt)
    print(x) 
    ~~~~

#### Metacharacters
- ##### [ ]
  - A set of characters
    ~~~~
    "[a-m]"
    ~~~~
- ##### \
  - Signals a special sequence (can also be used to escape special characters)
    ~~~~
    "\d"
    ~~~~
- ##### .
  - Any character (except newline character)
    ~~~~
    "he..o"
    ~~~~
- ##### ^
  - Starts with
    ~~~~
    "^hello"
    ~~~~
- ##### $
  - Ends with
    ~~~~    
    "world$"
    ~~~~
- ##### *
  - Zero or more occurrences
    ~~~~
    "aix*"
    ~~~~
- ##### +
  - One or more occurrences
    ~~~~
    "aix+"
    ~~~~
- ##### {}
  - Exactly the specified number of occurrences
    ~~~~
    "al{2}"
    ~~~~
- ##### |
  - Either or
    ~~~~
    "falls|stays"
    ~~~~
- ##### ()
  - Capture and group

#### Sets
A set is a set of characters inside a pair of square brackets [] with a special meaning:
- ##### [arn]
  - Returns a match where one of the specified characters (**a**, **r**, or **n**) are present
- ##### [a-n]
  - Returns a match for any lower case character, alphabetically between **a** and **n**
- ##### [^arn]
  - Returns a match for any character EXCEPT **a**,**r**, and **n**
- ##### [0123]
  - Returns a match where any of the specified digits (**0**, **1**, **2**, or **3**) are present
- ##### [0-9]
  - Returns a match for any digit between **0** and **9**
- ##### [0-5][0-9]
  - Returns a match for any two-digit numbers from **00** and **59**
- ##### [a-zA-Z]
  - Returns a match for any character alphabetically between **a** and **z**, lower case OR upper case
- ##### [+]
  - In sets, **+**, *, **.**, **|**, **()**, **$**,**{}** has no special meaning, so **[+]** means: return a match for any **+** character in the string
