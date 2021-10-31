# Web Scraping
![Web Scraping](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTBV834mYMO8gJ5utuWjjJzNaO0M6litvOGvg&usqp=CAU)

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. In this article, we will go through an easy example of how to automate downloading hundreds of files from the New York MTA. This is a great exercise for web scraping beginners who are looking to understand how to web scrape. Web scraping can be slightly intimidating, so this tutorial will break down the process of how to go about the process.

### Important notes about web scraping:
- Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.
- Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.

## Python Code
We start by importing the following libraries.

```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

Next, we set the url to the website and access the site with our requests library.

```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```
If the access was successful, you should see the following output:
![success](https://miro.medium.com/max/518/1*fyqRGzG8IbhhjxF2Q5MU_Q.png)

Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure.

```
soup = BeautifulSoup(response.text, “html.parser”)
soup.findAll('a')
```
This code gives us every line of code that has an `<a>` tag. The information that we are interested in starts on line 38 as seen below. That is, the very first text file is located in line 38, so we want to grab the rest of the text files located below.

![txt](https://miro.medium.com/max/728/1*G6YulYb5rczkVvmn7nbQ6g.png)

extract the actual link that we want

```
one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
```

# Beautiful Soup
Beautiful Soup is a Python library designed for quick turnaround projects like screen-scraping.

![Beautiful Soup](https://miro.medium.com/max/1400/0*5l1YDbdnkWmQwDU5.jpg)


Beautiful Soup is a Python package for parsing HTML and XML documents. It creates a parse tree for parsed pages that can be used to extract data from HTML, which is useful for web scraping.


      
© Haneen Hashlamoun
