[Back](../libraries.md)
##### [Web Scraping](../web_scraping.md)

# Selenium
---

Selenium is library that can be useful when scraping the web. Unlike the other libraries, Selenium wasn’t originally designed for web scraping. First and foremost, Selenium is a web driver designed to render web pages like your web browser would for the purpose of automated testing of web applications.

- Install Selenium
```python
pip install selenium
```
- Use Selenium
```python
from selenium import webdriver
``` 
- Create a Beautiful Soup object from page.
```python
soup = BeautifulSoup(response.content, 'html.parser')
``` 
- Functions find() and find_all().
Find() for get one result and find_all() for get all results.tt
```python
body = soup.find('body')
div = soup.find_all('div')
``` 
- 
```python

``` 
- 
```python

``` 
- 
```python

``` 