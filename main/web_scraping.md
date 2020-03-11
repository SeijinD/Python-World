[Back](../README.md)

# Web Scraping
---

- ### Why Web Scraping?
    Web scraping is used to collect large information from websites. But why does someone have to collect such large data from websites? To know about this, let’s look at the applications of web scraping:
    - Price Comparison
    - Email address gathering
    - Social Media Scraping
    - Research and Development
    - Job listings
- ### Why Python For Web Scraping?
    Here is the list of features of Python which makes it more suitable for web scraping.
    - Ease of Use
    - Large Collection of Libraries
    - Dynamically typed
    - Easily Understandable Syntax
    - Small code, large task
    - Community
- ### What is Web Scraping?
    Web scraping is an automated method used to extract large amounts of data from websites. The data on the websites are unstructured. Web scraping helps collect these unstructured data and store it in a structured form. There are different ways to scrape websites such as online Services, APIs or writing your own code.
- ### Libraries for Web Scraping
    - #### Requests
        Requests is a python library designed to simplify the process of making HTTP requests.This is highly valuable for web scraping because the first step in any web scraping workflow is to send an HTTP request to the website’s server to retrieve the data displayed on the target web page.
        - Install Requests
        ```python
        pip install requests
        ```
        - Use Requests
        ```python
        import requests
        ```
        - You can make a Get request with method get().
        ```python
        requests.get('https://www.wikipedia.gr')
        ``` 
        - You can use many times the results of get() with use a variable.
        ```python
        response = requests.get('https://www.wikipedia.gr')
        ``` 
        - The first bit of information that you can gather from Response is the status code. A status code informs you of the status of the request.
        ```python
        if response.status_code == 200:
            print('Success!')
        elif response.status_code == 404:
            print('Not Found.')
        ```
        - To see the response’s content in bytes, you use .content.
        ```python
        response.content
        ``` 
        - If you want to convert them into a string using a character encoding such as UTF-8. You can access with the .text.
        ```python
        response.text
        ``` 
        - To see the response’s content in json, you use .json.
        ```python
        response.json
        ``` 
        - The response headers can give you useful information, such as the content type of the response payload and a time limit on how long to cache the response. To view these headers, access  .headers.
        ```python
        response.headers
        ``` 
        - When your browser is connected to a website, a User-Agent field is included in the HTTP header. The data of the header field varies from browser to browser. This information is used to serve different websites to different web browsers and different operating systems.
        ```python
        header = {'User-agent':'Mozilla/5.0'}
        response = requests.get('https://www.wikipedia.gr', headers=header)
        ``` 
    - #### BeautifulSoup
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
    - #### Selenium
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
    - #### Scrapy (Web Scraping Framework)
        Scrapy is an open source python framework built specifically for web scraping by Scrapinghub co-founders Pablo Hoffman and Shane Evans.
        It means that Scrapy is a fully fledged web scraping solution that takes a lot of the work out of building and configuring your spiders, and best of all, it seamlessly deals with edge cases that you probably haven’t thought of yet.
        Within minutes of installing the framework, you can have a fully functioning spider scraping the web. Out of the box, Scrapy spiders are designed to download HTML, parse and process the data and save it in either CSV, JSON or XML file formats.
        - Install Scrapy
        ```python
        pip install scrapy
        ```
        - Use Scrapy
        ```python
        import scrapy
        ```
    - #### Lxml
        lxml is a Python library which allows for easy handling of XML and HTML files, and can also be used for web scraping. There are a lot of off-the-shelf XML parsers out there, but for better results, developers sometimes prefer to write their own XML and HTML parsers. This is when the lxml library comes to play. The key benefits of this library are that it's ease of use, extremely fast when parsing large documents, very well documented, and provides easy conversion of data to Python data types, resulting in easier file manipulation.
        - Install Lxml
        ```python
        pip install lxml
        ```
        - Use Lxml
        ```python
        from lxml import etree
        ``` 
    - #### Pandas
        Pandas is an open-source, BSD-licensed Python library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.
        - Install Pandas
        ```python
        pip install pandas
        ```
        - Use Pandas
        ```python
        import pandas as pd
        ``` 

- ### Examples