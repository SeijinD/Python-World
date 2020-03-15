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
    - #### [Requests](extends_libraries/requests.md) (Full Tutorial)
        Requests is a python library designed to simplify the process of making HTTP requests.This is highly valuable for web scraping because the first step in any web scraping workflow is to send an HTTP request to the website’s server to retrieve the data displayed on the target web page.

    - #### [BeautifulSoup](extends_libraries/beautifulsoup.md) (Full Tutorial)
        Unlike Requests, BeautifulSoup is a python library designed to parse data, i.e., to extract data from HTML or XML documents.
        Because BeautifulSoup can only parse the data and can’t retrieve the web pages themselves, it is often used with the Requests library. In situations like these, Requests will make the HTTP request to the website to retrieve the web page, and once it has been returned, BeautifulSoup can be used to parse the target data from the HTML page.

    - #### [Selenium](extends_libraries/selenium.md) (Full Tutorial)
        Selenium is library that can be useful when scraping the web. Unlike the other libraries, Selenium wasn’t originally designed for web scraping. First and foremost, Selenium is a web driver designed to render web pages like your web browser would for the purpose of automated testing of web applications.

    - #### [Scrapy (Web Scraping Framework)](extends_libraries/scrapy.md) (Full Tutorial)
        Scrapy is an open source python framework built specifically for web scraping by Scrapinghub co-founders Pablo Hoffman and Shane Evans.
        It means that Scrapy is a fully fledged web scraping solution that takes a lot of the work out of building and configuring your spiders, and best of all, it seamlessly deals with edge cases that you probably haven’t thought of yet.
        Within minutes of installing the framework, you can have a fully functioning spider scraping the web. Out of the box, Scrapy spiders are designed to download HTML, parse and process the data and save it in either CSV, JSON or XML file formats.

    - #### [Lxml](extends_libraries/lxml.md) (Full Tutorial)
        lxml is a Python library which allows for easy handling of XML and HTML files, and can also be used for web scraping. There are a lot of off-the-shelf XML parsers out there, but for better results, developers sometimes prefer to write their own XML and HTML parsers. This is when the lxml library comes to play. The key benefits of this library are that it's ease of use, extremely fast when parsing large documents, very well documented, and provides easy conversion of data to Python data types, resulting in easier file manipulation.

    - #### [Pandas](extends_libraries/pandas.md) (Full Tutorial)
        Pandas is an open-source, BSD-licensed Python library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.

- ### Examples