# BeautifulSoup
---

Unlike Requests, BeautifulSoup is a python library designed to parse data, i.e., to extract data from HTML or XML documents.
Because BeautifulSoup can only parse the data and can’t retrieve the web pages themselves, it is often used with the Requests library. In situations like these, Requests will make the HTTP request to the website to retrieve the web page, and once it has been returned, BeautifulSoup can be used to parse the target data from the HTML page.

- Install BeautifulSoup
```python
pip install beautifulsoup4
```
- Use BeautifulSoup
```python
from bs4 import BeautifulSoup
``` 