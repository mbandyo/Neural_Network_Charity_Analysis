# Neural Network Charity Analysis
This project is designed to assess potential successful ventures through AlphabetSoup funding. 

The model would create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
## Data

A a CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years would be used as raw data.  Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

## Data Processing
After reading raw data from the charity_data.csv file, the data goes through first scan to ensure only data that could be relevant to grouping is handed to machine learning logic. The following steps are used to scrub data for use:
* Drop identification columns 'EIN' and 'NAME'.
* Determine tne number of unique values in each remaiing columns.
* For number of unique values less than 1800, bucketing is used to make group sizes reasonable.
* Data was mapped to ensure all the columns have numerical representation.
* Mapped and scrubbed data is merged into a dataframe.
* Data is split into train and test datasets.

## Model Design and Execution
For initial model, the following layers were executed:
* First hidden layer consisted of 80 nodes and rectified linear (relu) activation function.
* Second hidden layer consisted of 30 nodes and rectified linear (relu) activation function.
* Output layer uses sigmoid activation function.


