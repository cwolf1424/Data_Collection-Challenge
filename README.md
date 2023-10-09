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

--------------------------------------------------
Step 1: Visit the Website (Mars News)
--------------------------------------------------
This section was provided by the starter file.

--------------------------------------------------
Step 2: Scrape the Website (Mars News)
--------------------------------------------------

The following section:

    news_text=news_soup.get_text(strip=True)

Was using a method I got from:

    https://www.educative.io/answers/how-to-use-gettext-in-beautiful-soup

--------------------------------------------------
Step 3: Store the Results (Mars News)
--------------------------------------------------

The following section:

    # Convert to JSON
    articles_json=json.dumps(articles_details, indent=4)
    print(articles_json)

and:

    # Export to JSON file
    with open("articles_data.json", "w") as outfile:
    outfile.write(articles_json)

Used the method layed out here:
https://www.geeksforgeeks.org/reading-and-writing-json-to-a-file-in-python/


--------------------------------------------------
Setup (Mars Weather)
--------------------------------------------------


