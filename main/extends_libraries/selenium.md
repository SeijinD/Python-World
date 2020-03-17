[Back](../extends_libraries.md)
##### [Web Scraping](../web_scraping.md)

# Selenium
---

Selenium is library that can be useful when scraping the web. Unlike the other libraries, Selenium wasn’t originally designed for web scraping. First and foremost, Selenium is a web driver designed to render web pages like your web browser would for the purpose of automated testing of web applications.

- #### Install Selenium
```python
pip install selenium
```
- #### Use Selenium
```python
from selenium import webdriver
``` 
- #### Driver setup
[Chrome Link](https://sites.google.com/a/chromium.org/chromedriver/downloads)
[Firefox Link](https://github.com/mozilla/geckodriver/releases)
[Opera Link](https://github.com/operasoftware/operachromiumdriver/releases)
[Edge Link](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/)
```python
# Chrome:
chrome_driver = webdriver.Chrome(“Chrome Driver Path”)
# Firefox:
firefox_driver = webdriver.Firefox(“Firefox Driver Path”)
# Opera:
opera_driver = webdriver.Opera(“Opera Driver Path”)
# Edge:
edge_driver = webdriver.Edge(“Edge Driver Path”)
# Safari
safari_driver = webdriver.Safari() # The SafariDeriver is integrated in Safari.
``` 

- #### Open A Website
```python
url = "https://www.example.com"
driver.get(url)
```

- #### Find An Elements
```python
# Example
<a href="/sign-up" id="register" name="register" class="cta nav-link">Sign Up</a>

# Find Element By ID
id_name = 'register'
element = driver.find_element_by_id(id)
# Find Element By Class
class_name = 'register'
element = driver.find_element_by_class_name(class_name)
# Find Element By Name
name = 'register'
element = driver.find_element_by_id(name)
# Find Element By Tag
tag_name = 'a'
element = driver.find_element_by_tag_name(tag_name)
# Find Element By Link Text
link_text = 'Sign Up'
element = driver.find_element_by_link_text(link_text)
# Find Element By Partial Link Text
partial_link_text = 'Sign'
element = driver.find_element_by_partial_link_text(partial_link_text)
# Find Element By CSS Selector
css_selector_1 = '*[attribute="attribute_value"]'
css_selector_2 = 'a[href="/sign-up"]'
element = driver.find_element_by_css_selector(css_selector_1)
# Find Element By XPath
xpath_1 = '//a[@href = "/sign-up"]'
element = driver.find_element_by_xpath(xpath_1)
```

- #### Click On An Element
```python
id_name = 'register'
element = driver.find_element_by_id(id_name)
element.click()
```

- #### Write Text Inside An Element
```python
id_name = 'email'
email = 'example@example.com'
element = driver.find_element_by_id(id_name)
element.send_keys(email)
```

- #### Select An Option
```python
# Example
<select id="country">
    <option value="US">United States</option>
    <option value="CA">Canada</option>
    <option value="MX">Mexico</option>
</select>
# Let's select United States. US

# You can use the visible text: 
id_name = 'country'
element = driver.find_element_by_id(id_name)
select_element = Select(element)
select_element.select_by_visible_text('United States')

# You can use the value: 
id_name = 'country'
element = driver.find_element_by_id(id_name)
select_element = Select(element)
select_element.select_by_value('US')

# You can also use the index: 
id_name = 'country'
element = driver.find_element_by_id(id_name)
select_element = Select(element)
select_element.select_by_index(0)
```

- #### Get first element from list
```python
id_name = 'register'
list_of_elements = driver.find_elements_by_id(id_name)
first_element = list_of_elements[0]
```

- #### Take A Screenshot
```python
path = 'C:/example/screenshots/example_1.png'
driver.save_screenshot(path)
```

- #### Upload A File
```python
# Example
<input type="file" multiple="" id="upload_button">

file_path = 'C:/example/files/example_1.pdf'
id_name = 'upload_button'
element = driver.find_element_by_id(id_name)
element.send_keys(file_path)
```

- #### Execute JavaScript
```python
js_code = 'document.getElementById("pop-up").remove()'
driver = execute_script(js_code)
```

- #### Close Tab / Alert
```python
driver.close() # Close Tab
driver.switch_to.alert.accept() # Close Alert
```

- #### Navigation Page
```python
driver.refresh() # Refresh
driver.back() # Go Privius Page
driver.forward() # Go Next Page
```

- #### Hover
```python
id_name = "register"
the_element = driver.find_element_by_id(id_name)
hover = ActionChains(driver).move_to_element(the_element)
hover.perform()
```

- #### Click with offset
```python
id_name = "register"
the_element = driver.find_element_by_id(id_name)
x = 30
y = 20
offset = ActionChains(driver).move_to_element_with_offset(the_element,x,y)
offset.click()
offset.perform()
```

- #### Right Click
```python
id_name = "register"
the_element = driver.find_element_by_id(id_name)
right_click = ActionChains(driver).context_click(the_element)
right_click.perform()
```

- #### Press Key
```python
id_name = 'register'
element = driver.find_element_by_id(id_name)
element.send_keys(Keys.RETURN)
```

- #### Checkbox/Radio
```python
# Check if it is selected
driver.find_element(:id, 'CheckBox').selected?
# Select the element
driver.find_element(:id, 'CheckBox').click
# Deselect the element
driver.find_element(:id, 'CheckBox').clear
```

- ####  Drag and drop
```python
element_to_drag_id = 'ball'
target_element_id = 'goal'
element_to_drag = driver.find_element_by_id(element_to_drag_id)
target_element = driver.find_element_by_id(target_element_id)
ActionChains(driver).drag_and_drop(element_to_drag_id, target_element).perform()
```

- #### Get Page Source
```python
the_page_source = driver.page_source
```

- #### Get Cookies / Delete Cookies
```python
# Get Coukies
cookies_list = driver.get_cookies()
cookie_item = 'shopping_cart'
# Delete one cookie
driver.delete_cookie(cookie_item)
# Delete all cookies
driver.delete_all_cookies()
```

- #### Set window size
```python
driver.set_window_size(1000, 800)
```

- #### Configure Page Load Timeout
```python
driver.set_page_load_timeout(20)
```

- #### Configure Element Load Timeout
```python
from selenium.webdriver.support.ui import WebDriverWait

id_name = 'register'
WebDriverWait(driver,10).until(EC.presence_of_element_located((By.ID, id_name)))
```