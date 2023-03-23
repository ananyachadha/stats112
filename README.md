Hi! 
The data I used in the data folders are a free-trial of paid data, from the YesEnergy API. 
I also used a free trial of meteomatics API and weather APIs in my scripts directly. 
As a result, this is a private repo, since I don't want to expose paid data. 

STRUCTURE: 
1. Data Collection
2. Data Cleaning
3. Data Exploration
4. Machine Learning
5. Final Machine Learning 
(In Final ML, we run the pipeline in a giant for loop, to loop through many nodes. 
This lets us get accuracy scores for many nodes by running just one file.)
The combined file merges collection, cleaning and ML. It omits exploration since we are running a known pipeline. 





1-Getting Data.ipynb
put data in spreadsheets to be imported into data cleaning file.
data from Yesenergy for prices
data from sunrise sunset API
data from meteomatics API
data from synoptic labs API
data from airport lat/long API

2-Cleaning Data.ipynb
clean it up
joins
change variable names
removes $, commas, nans
converts timezones from utc to pst

3-Data Exploration.ipynb
graph how price has changed over time
graph price throughout the day
graph price over the months
graph price spread through day
price spread through months

4-Machine Learning.ipynb
predict price spread given input variables
clean "return $/MW" column to just be binary buy or sell if it's positive or negative
predict buy or sell given input variables

5- CombinedMLPipeline.ipynb is where the magic happens!
Here we combine ALL files 1, 2, and 4 to create a for loop to iterate through many nodes.


Data: in this folder we have price data for each node. I got this from YesEnergy. It was my only non-api data. 
Intermediate Data: a lot of my data is from APIs and they are saved as csvs through the process. If you want to check in what a CSV looks like, it's probably in the intermediate data folder.

