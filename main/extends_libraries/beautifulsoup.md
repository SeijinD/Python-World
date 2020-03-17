[Back](../extends_libraries.md)
##### [Web Scraping](../web_scraping.md)

# BeautifulSoup
---

Unlike Requests, BeautifulSoup is a python library designed to parse data, i.e., to extract data from HTML or XML documents.
Because BeautifulSoup can only parse the data and can’t retrieve the web pages themselves, it is often used with the Requests library. In situations like these, Requests will make the HTTP request to the website to retrieve the web page, and once it has been returned, BeautifulSoup can be used to parse the target data from the HTML page.

- #### Install BeautifulSoup
```python
pip install beautifulsoup4
```

- #### Use BeautifulSoup
```python
from bs4 import BeautifulSoup
``` 

- #### Make Soup Object
```python
soup = BeautifulSoup(page.text, 'html.parser')
soup = BeautifulSoup(page.content, 'html.parser')
```

- #### Output From Soup Object
```python
# HTML
print(soup.prettify()) # Pretty Print
print(str(soup)) # Non-Pretty Print
print(soup) # Non-Pretty Print
# String (Bad Way)
print(soup.get_text())
```

- #### Search
```python
# CSS Selector
soup.select('p') # Select all "p" tags.
soup.select('p nth-of-type(3)') # Select 3rd child of "p".
soup.select('div > p') # Select all "p" tags down from "div" tag.
soup.select('a[href]') # Select all "a" tags with attribute "href". 

# Attribute Value (^,$,*)
soup.select('a[href="https://www.iee.ihu.gr"]') # Select "a" tag with attribte "href and it has this link.
soup.select('a[href^="https://www.iee.ihu.gr"]') # Select "a" tag with attribte "href and start with this link.
soup.select('a[href$="https://www.iee.ihu.gr"]') # Select "a" tag with attribte "href and end with this link.
soup.select('a[href*="https://www.iee.ihu.gr"]') # Select "a" tag with attribte "href and there is this link.

# Find / Find_All
# find_all(name, attrs, recursive, string, limit, **kwargs)
soup.find('p') # Find first "p" tag.
soup.find_all('p') # Find all "p" tags.
soup.find_all(re.compile("^p")) # Find all "p" tags with regex.
soup.find_all(["a","p"]) # Find all tags in list (a,p).
soup.find_all("p", "title") # Find all "p" tags with attribute "title".
soup.find_all(id="id1") # Find all elements with this id.
soup.find_all(class_="class1") # Find all elements with this class.
soup.find_all("div", class_="class1") # FInd all "div" tags with this class.
soup.find_all("div", {"class": "class1"}) # FInd all "div" tags with this class.
```

- #### Navigation
```python
soup       # All Html file.
soup.html  # All Html file.
soup.head  # All elements in head tag.
soup.body  # All elements in body tag.
soup.title # Title Tag.
soup.a     # All "a" tags. | soup.find_all("a") is same.
soup.div.a # All "a" tags down from "div" tag.

# Children = Contents = Descendants
# All elements down from "head" tag.
soup.head.contents 
# All elements down from "head" tag.
for child in head_tag.descendants:
  print(child)
# All elements down from "head" tag.
for child in head_tag.children:
  print(child)

soup.head.string # If it has only one child, it show it. If it has many child, it show None.
for string in soup.stripped_strings: # Whitespace removed strings.
  print(repr(string))

# Parent/Parents
# The parent element from "title" tag.
soup.title.parent
# The parents elements from "div" tag.
soup.div.parents
```