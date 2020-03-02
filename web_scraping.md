# Web Scraping
---

- ### Why Web Scraping?

- ### Why Python For Web Scraping?

- ### What is Web Scraping?

- ### Libraries for Web Scraping
    - #### Requests
        Requests is a python library designed to simplify the process of making HTTP requests.This is highly valuable for web scraping because the first step in any web scraping workflow is to send an HTTP request to the website’s server to retrieve the data displayed on the target web page.
        - Install Requests
        ~~~~
        pip install requests
        ~~~~
        - Use Requests
        ~~~~
        import requests
        ~~~~         
    - #### BeautifulSoup
        Unlike Requests, BeautifulSoup is a python library designed to parse data, i.e., to extract data from HTML or XML documents.
        Because BeautifulSoup can only parse the data and can’t retrieve the web pages themselves, it is often used with the Requests library. In situations like these, Requests will make the HTTP request to the website to retrieve the web page, and once it has been returned, BeautifulSoup can be used to parse the target data from the HTML page.
        - Install Requests
        ~~~~
        pip install beautifulsoup4
        ~~~~
        - Use Requests
        ~~~~
        from bs4 import BeautifulSoup
        ~~~~ 
    - #### Selenium
        Selenium is library that can be useful when scraping the web. Unlike the other libraries, Selenium wasn’t originally designed for web scraping. First and foremost, Selenium is a web driver designed to render web pages like your web browser would for the purpose of automated testing of web applications.
    - #### Scrapy (Web Scraping Framework)
        Scrapy is an open source python framework built specifically for web scraping by Scrapinghub co-founders Pablo Hoffman and Shane Evans.
        It means that Scrapy is a fully fledged web scraping solution that takes a lot of the work out of building and configuring your spiders, and best of all, it seamlessly deals with edge cases that you probably haven’t thought of yet.
        Within minutes of installing the framework, you can have a fully functioning spider scraping the web. Out of the box, Scrapy spiders are designed to download HTML, parse and process the data and save it in either CSV, JSON or XML file formats.
    - #### Lxml

    - #### Pandas


- ### Examples