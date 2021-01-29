# Wrnagling_Data_Worksheet
This works sheet should cover step-by-step all details covering 'assess' and 'clean' process for data Wrangling


# Introduction
Real-world data rarely comes clean. Using Python and its libraries, we will gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. 
We will document our wrangling efforts in a Jupyter Notebook, plus showcase them through analyses and visualizations using Python (and its libraries) and/or SQL.

The dataset that we will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user [@dog_rates](https://twitter.com/dog_rates), also known as WeRateDogs. 

WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for you to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. More on this soon.

## Important notes
- We will use both visual and programatic assessment for the data
- We will focus on Programmatic: Data Cleaning 
  - Define
  - Code 
  - Test
- This will help us plot and recognise quality issues and tidiness isses within the data 
- Then we will go ahead and mark all our quality and tidy observation in this worksheet



# Software Needed


The following packages (libraries) is needed:
- pandas
- NumPy
- requests
- tweepy
- json
- os


We need to be able to create written documents that contain images and we need to be able to export these documents as PDF files. This task can be done in a Jupyter Notebook, but you might prefer to use a word processor like [Google Docs](https://www.google.com/docs/about/), which is free, or Microsoft Word.
A text editor, like [Sublime](https://www.sublimetext.com/), which is free, will be useful but is not required.



## DataFrame files 
This should include three files, that we will intent to clean and then combine or merge at a later stage in this worksheet
- patients 
- treatments 
- adverse_reactions 


# Project Details

Our tasks in this project doe Data wrangling, consists of:
- Gathering data (downloadable file in the Resources tab in the left most panel of your classroom and linked in step 1 below).
- Assessing data
- Cleaning data
- Storing, analyzing, and visualizing your wrangled data
- Reporting on 1) your data wrangling efforts and 2) your data analyses and visualizations



# Summary:

The Data for Twitter_archives, image_predictions and tweets.text requires a lot of cleaning, from the datatype to the validy, acuracy and tidiness of the data provided in the first files.

There are more than 14 quality issues that need to be cleaned. And half of it need to be done by manually;
Probably one of the best way to clean data for dog names and their numerator and deminator numbers is manuualy, row by row. By checking and varifying text and tweets correlated with the scores on numerator and denominators a=to be able to clean its data.

Also there is the p2, p3, p2_dog, p3_dog that can be dropped easily from the master file, as their confidence level is less than p1_dog. We have measured and quantified that programmically. This should not affect the end result of our analysis.

To save time and specifically for the rating columns, I have used programmatic way to replace the mean with the wrong figures.
I have also used some logic doign that especially for the numerator figures below 10. 
You will notice here that there 440 rows with numerators below 10, but only fewer for those below 5 so I have used the lower mean number using the lower braket below the total mean level.


Overall, this was the most challenging and demonstrative worksheet I have learned a lot, slept a less, researched even more, but I hope I was able to cover all requirements for worksheet.


thanks
