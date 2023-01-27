# Web-Scraping-Challenge

# Unit 12 Homework: Mission to Mars

In this assignment, you will build a web application that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page. The following information outlines what you need to do.

# Instructions
# Deliverable 1: Scrape Titles and Preview Text from Mars News
Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. You will work in this code as you follow the steps below to scrape the Mars News website.

Use automated browsing to visit the Mars NASA news site Links to an external site.. Inspect the page to identify which elements to scrape.

HINT
Create a Beautiful Soup object and use it to extract text elements from the website.

Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:

Store each title-and-preview pair in a Python dictionary. And, give each dictionary two keys: title and preview. An example is the following:

{'title': "Mars Rover Begins Mission!",
      'preview': "NASA's Mars Rover begins a multiyear mission to collect data about the little-explored planet."}
Store all the dictionaries in a Python list.

Print the list in your notebook.

![image](https://user-images.githubusercontent.com/111756299/214957980-79f10924-d7df-4b2a-bdf8-32c426626631.png)


Optionally, store the scraped data in a file or database (to ease sharing the data with others). To do so, export the scraped data to either a JSON file or a MongoDB database.

# Deliverable 2: Scrape and Analyze Mars Weather Data
Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.

Use automated browsing to visit the Mars Temperature Data Site Links to an external site.. Inspect the page to identify which elements to scrape. Note that the URL is https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html.

HINT
Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.

Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:

id: the identification number of a single transmission from the Curiosity rover

terrestrial_date: the date on Earth

sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars

ls: the solar longitude

month: the Martian month

min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)

pressure: The atmospheric pressure at Curiosity's location

Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.

HINT
Analyze your dataset by using Pandas functions to answer the following questions:

1. How many months exist on Mars?
![image](https://user-images.githubusercontent.com/111756299/214963988-fc4dad9c-9b13-444a-ae51-75edef762126.png)

2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
![image](https://user-images.githubusercontent.com/111756299/214964533-ed527fbb-e5bd-429d-9131-00b110eaabf1.png)

3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
   Find the average the minimum daily temperature for all of the months.
   
   ![image](https://user-images.githubusercontent.com/111756299/214965325-dcc8ddd3-955a-4016-83ba-0f96b33e8306.png)

   
   Plot the results as a bar chart.
   
![image](https://user-images.githubusercontent.com/111756299/214965442-4165f386-555f-424a-949e-a906df628be1.png)

![image](https://user-images.githubusercontent.com/111756299/214968077-0cc0bc90-799d-4710-bbe8-56c3ca2a3358.png)


4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
Find the average the daily atmospheric pressure of all the months.

![image](https://user-images.githubusercontent.com/111756299/214968341-539055d7-4d5e-427c-983c-48918de89503.png)

Plot the results as a bar chart.

![image](https://user-images.githubusercontent.com/111756299/214970959-1fc6b300-8984-4641-9592-91a123f49920.png)


5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
Consider how many days elapse on Earth in the time that Mars circles the Sun once.
Visually estimate the result by plotting the daily minimum temperature.

![image](https://user-images.githubusercontent.com/111756299/214973023-fe012a93-6ed5-4478-aee6-116d0ad30be0.png)

The data is organised to be able to obtain peak temperatures. The two peak temperatures are on sols 1582 and 926 respectively. The difference between these two days is 656. Therefore, we can assume that a Mars year is approximately 656 earth days. On google, a Mars year is said to be 687 earth days long. Therefore, as shown with the analysis, there is an insginificant difference between the dataset values and the estimated days in a year on Mars from a google search.

Export the DataFrame to a CSV file.
