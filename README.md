# Can we Predict San Fransisco Park Scores based on their neighborhoods?


## Purpose:

Thoughout San Francisco there are more than 200 parks. Each park in the city is given a certain rating that indicates the condition of the park. By analyzing the surrounding factors of the neighborhood a park is located in, a correlation can be identified between parks scores and the quality of the facilities in surrounding areas.

## Data:
Downloaded and analyzed different kinds of data sets which included one for park scores, one for evictions, and one for crimes. All of these sets were found on datasf.org

Also I wanted to find a correlation between park scores and the reputation/rank of schools located in the same area. There was no downloadable data set that could be collected to analyze and compare school ranks with parks based on location, so the data was obtained by scraping it from different websites.

The first website that I tried to scrape was the Nook website (which gives a list of San Francisco school and their ratings) using selenium. However, the Cloudfare element detected the robot accessing the website and prevented me from downloading the data. So, the next method was to download a list of addresses from the sf edu website of different elementary, middle, and high school in the area. After collecting the addresses, I wanted to see the neighborhood each school was located in. To do this, I used open-source maps to find the coordinates of the address and compared it with the different neighborhoods to see which one contained that coorrdinate using geopandas.

## Libraries used:
- Pandas
- Geopandas
- Shapely
- Numpy
- Matplotlib
- Requests
- Selenium

## A few Interesting Observations:

As we can see the graph below, most parks have a score between 60 and 90. Interestingly, Seward and Crocker Amazon Playground seems outliers with scores of ... and ... respectively.


Specific information about data:
#Park ID is another way to find the park
#PSA stands for Park Service Area
#Name of Park
#FQ - FY: Fiscal Year, Q: Quarter; 
#Q1: July-Sept, Q2: Oct-Dec, Q3: Jan-March, Q4: April-June
#park scores are recorded from FY05 (fiscal year 2005) Q3 (third quarter of the year) 
#until FY14 (fiscal year 2014) Q4 (fourth/last quarter of the year)
#Scores: 0-1 (0% to 100%); higher number [closer to 1] means the park has a better score
#https://sfcontroller.org/sites/default/files/FileCenter/Documents/4857-Parks%20Report_10%2023%2013_FINAL.pdf 
#https://sfcontroller.org/park-scores
#https://data.sfgov.org/Culture-and-Recreation/Annual-Park-Evaluation-Scores-2015-2019/r33y-seqv

Graphs:

***Graph 1: Park and their respective Park Scores from data.sf ***

<img width="434" alt="Screen Shot 2022-11-10 at 2 13 35 PM" src="https://user-images.githubusercontent.com/90660851/201217102-6c0cd224-de1d-4bc2-bd86-d24d6a606940.png">



Interestingly, the parks located in ... neighborhood seem to fare a lot better.


It's also the neighborhoods with the best ...


Which leads me to believe that the score of a park/neighborhood ...

