[Back](../extends_libraries.md)
##### [Web Scraping](../web_scraping.md)

# Requests
---

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