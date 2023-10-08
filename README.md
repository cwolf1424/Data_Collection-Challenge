# Data_collection-challenge
Challenge assignment for Data Collection

Data for this challenge was from the folowing sites provided in the instructions:

https://static.bc-edx.com/data/web/mars_news/index.html



Layout for assignment came from starter file.

Specific sections using sources listed below:

--------------------------------------------------
Setup (Mars News)
--------------------------------------------------

I had trouble with getting the remote browser to work. Ian from the AskBCS team provided the following to assist with setup:

    executable_path = {'executable_path': ChromeDriverManager().install()}
    browser = Browser('chrome', **executable_path, headless=False)

The following section:

    news_text=news_soup.get_text(strip=True)

Was using a method I got from:

    https://www.educative.io/answers/how-to-use-gettext-in-beautiful-soup

--------------------------------------------------
Exploratory Precipitation Analysis (Climate_Analysis)
--------------------------------------------------

The following section:

