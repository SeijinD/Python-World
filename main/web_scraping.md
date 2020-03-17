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

- ### Examples
```python
# Example 1:
import requests
from bs4 import BeautifulSoup
import pandas as pd # Pandas is useful library. (Go Extends Liraries)

page = requests.get('https://meteo.gr/lab/book/index.cfm?city_id=1')
soup = BeautifulSoup(page.content, 'html.parser')

# Lists to store the scraped data in
days = []
temperatures = []
# Extract data from individual dayblock
for block in soup.find_all(class_ = 'dayblock'):
    day = block.find(class_ = 'subheader_calendar')
    # Data Number and Month Name
    dom = block.find(class_ = 'datenumber_calendar').get_text()
    month = block.find(class_ = 'month_calendar').get_text()
    daystr = f"{dom} {month}"
    days.append(daystr)
    # Low and High Temperature
    hightemp = block.find(class_ = 'hightemp').get_text()
    lowtemp = block.find(class_ = 'lowtemp').get_text()
    tempstr = f"{lowtemp} {hightemp}"
    temperatures.append(tempstr)

# Print in Table with Pandas
weather_table = pd.DataFrame({
    'Days' : days,
    'Temperatures' : temperatures
})
# Extract to the csv file
weather_table.to_csv('week_weather.csv')

# ==================================================
# Example 2:
from selenium import webdriver
import csv

MAX_PAGE_NUM = 5
MAX_PAGE_DIG = 3

with open('result.csv', 'w', encoding='utf8') as f:
    f.write("Buyers, Price \n")

# Set driver with Firefox webdriver
driver = webdriver.Firefox(executable_path="C:\\Python\\Tools\\geckodriver.exe")

# Make loop for run all pages
for i in range(1, MAX_PAGE_NUM + 1):
    page_num = (MAX_PAGE_DIG - len(str(i))) * "0" +str(i)
    url = "https://econpy.pythonanywhere.com/ex/" + page_num + ".html"
    driver.get(url)

    # Get buyers and prices by xpath
    buyers = driver.find_elements_by_xpath('//div[@title="buyer-name"]')
    prices = driver.find_elements_by_xpath('//span[@class="item-price"]')

    # Write all buyers+prices in result.csv
    with open('result.csv', 'a', encoding='utf8') as f:
        f.write("Page" + str(i) + "\n")
        for j in range(len(buyers)):
            f.write(str(j) + ") " + buyers[j].text + " : " + prices[j].text + "\n")
        
# Close driver
driver.close()
```