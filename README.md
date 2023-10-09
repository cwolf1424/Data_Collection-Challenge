# Data_collection-challenge
Challenge assignment for Data Collection

Data for this challenge was from the folowing sites provided in the instructions:

    https://static.bc-edx.com/data/web/mars_news/index.html

    https://static.bc-edx.com/data/web/mars_facts/temperature.html

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

I once again used the method Ian from AskBCS provided to get the remote browser to work.

--------------------------------------------------
Step 1: Visit the Website (Mars Weather)
--------------------------------------------------

This section was provided by the starter file.

--------------------------------------------------
Step 5: Analyze the Data (Mars Weather)
--------------------------------------------------
The method for the following section:

    plt.rcParams["figure.figsize"] = (10, 7)

Was provided by Robert from AskBCS.

The method for getting around the bug in MatPlotLib that would re-order the columns to numerical order, even after sorting the dataframe:

    plt.bar(sorted_tp_by_month_df.index,sorted_tp_by_month_df["min_temp"])
    plt.xticks(sorted_tp_by_month_df.index, sorted_tp_by_month_df["month"])

Was created with the assistance of Robert from AskBCS as well.

The following seciton:

    On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest. But it is always very cold there in human terms!

    Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.

    The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.

Was provided in the starter. 

My analysis came to the same conclusions, but I re-worded them