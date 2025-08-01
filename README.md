# Youtube Channel Scraping and Analysis

This data science project focuses on analyzing YouTube video titles to determine which words or phrases contribute to higher view counts. We'll be first scraping the nesscary data such as video titles, views, and video durations from youtube then perform data analysis. The goal is to gain insights into content strategy and audience engagement by examining how specific words in titles correlate with the popularity of videos.




## Features

- Scrapes video titles, views, and durations from any YouTube channel’s video page. 
- Automates dynamic page scrolling to capture data from all available videos.
- Parses and organizes data in a structured format for easy analysis.
- Reduces manual data collection effort, saving hours of work for large datasets.
## Features

- Scrapes video titles, views, and durations from any YouTube channel’s video page. 
- Automates dynamic page scrolling to capture data from all available videos.
- Parses and organizes data in a structured format for easy analysis.
- Reduces manual data collection effort, saving hours of work for large datasets.
## Tools Used

***Python:*** Programming language used for scripting.

***Selenium:*** Automates browser interaction to handle JavaScript-heavy content on YouTube.

***BeautifulSoup:*** Used to parse and extract relevant HTML elements.

***Chromedriver (or another appropriate WebDriver):*** Used by Selenium to interact with the browser.
## Installation

### Prerequisites
- Python 3.x installed on your machine.

- Selenium and BeautifulSoup libraries installed. Run the following command to install them:

```bash
  pip install selenium beautifulsoup4
```
- Download and install [ChromeDriver](https://developer.chrome.com/docs/chromedriver/downloads) or the appropriate WebDriver for your browser version. Ensure the WebDriver path is set correctly in the code.

### Import Libraries 


```python
import time 
from selenium import webdriver 
from selenium.webdriver.chrome.service import Service
from bs4 import BeautifulSoup 
import xlsxwriter
import pandas as pd 
import re
from tqdm import tqdm 
import nltk 
nltk.download('punkt') 
nltk.download('stopwords') 
from nltk.corpus import stopwords 
from nltk.tokenize import word_tokenize 
from nltk.stem.porter import PorterStemmer
from wordcloud import WordCloud 
import matplotlib.pyplot as plt 
import seaborn as sns
from collections import Counter
from sklearn.feature_extraction.text import CountVectorizer
import numpy as np
```

## Usage/Examples
In this example, I used my favorite YouTuber, [Ryan Trahan's](https://www.youtube.com/@ryan) channel, but you can replace the URL with any YouTube channel of your choice. However, make sure the URL follows a similar format to the one below.

```python
urls=['https://www.youtube.com/@ryan/videos']

```


## Data Exploration and Visualization

![image alt](https://github.com/Rwang0316/Youtube-Channel-Scraping-and-Analysis/blob/main/Media/WordCloud.png)
![image alt](https://github.com/Rwang0316/Youtube-Channel-Scraping-and-Analysis/blob/main/Media/Bar%20Graph.png)

| Key Word | Estimated Views  |   
| :-------- | :------- | 
| airline | 34000000.0 | 
| 3624         | 29000000.0 | 
| miles        | 29000000.0 | 
| traveled     | 29000000.0 | 
| parks | 27000000.0 | 
| seat                | 24000000.0 | 
| airbnbs             | 24000000.0 | 
| omg                 | 24000000.0 | 
| vision              | 23000000.0 | 

These words seem to be associated with high-view videos, with keywords related to travel experiences ("airline," "miles," "traveled") and specific topics (e.g., "theme parks," "airbnbs," "apple") generating the most engagement.

![image alt](https://github.com/Rwang0316/Youtube-Channel-Scraping-and-Analysis/blob/main/Media/Distribution.png)
![image alt](https://github.com/Rwang0316/Youtube-Channel-Scraping-and-Analysis/blob/main/Media/Scatter.png)

When examining the relationship between video duration and views, there was no clear linear correlation. This suggests that video length alone is not a significant factor in determining the popularity of a video.

***Key Observation:*** Mid-length videos (17 to 27 minutes) tend to perform well, while extremely long videos (over an hour) can still achieve millions of views if the content is engaging enough.
## Conclusion

This project identified critical factors that influence video viewership by analyzing video titles, durations, and views. Through comprehensive data scraping, preprocessing, and exploratory analysis, the project revealed key insights into the relationship between title keywords and viewership trends. The findings demonstrated that certain keywords and optimal video durations significantly contribute to higher engagement, providing a data-driven approach for optimizing content strategy.

## Furture Work
***Engagement Metrics Integration:*** Incorporating additional engagement data, such as likes, comments, and shares, would provide a more holistic view of video performance and help refine the relationship between viewer interaction and content strategy.

***Sentiment Analysis on Comments:*** Performing sentiment analysis on user comments can offer insights into viewer reactions and feedback, helping content creators understand audience sentiment and adjust content accordingly.

***Time-Series Analysis:*** Analyzing video performance trends over time could reveal patterns in viewership growth, audience retention, and seasonal content preferences, enabling more dynamic content planning.

***Thanks for reading!***
