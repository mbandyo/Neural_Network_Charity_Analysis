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
* Determine tne number of unique values in each remaiing columns. Following is the graph of count analysis.
* ![image](https://user-images.githubusercontent.com/31217096/204601163-1d4e8023-b908-4000-8033-1de8f2f091f5.png)
* For number of unique values less than 1800, bucketing is used to make group sizes reasonable.
* Data was mapped to ensure all the columns have numerical representation.
* Mapped and scrubbed data is merged into a dataframe.
* Data is split into train and test datasets.

## Model Design and Execution
For initial model, the following layers were executed:
* First hidden layer consisted of 80 nodes and rectified linear (relu) activation function.
* Second hidden layer consisted of 30 nodes and rectified linear (relu) activation function.
* Output layer uses sigmoid activation function.

The model was trained on training dataset and then tested on test data. The performance of the model was not very good with accuracy of 73%.

## Model Enhancement
In order to improve the model accuracy the model was fine tuned with the following steps:
* Increased number of bins (combining values less than 1000 occurrences only).
* Added two more hidden layers.
* Increased the final number of nodes in the hiddenlayers as 100 (hidden layer 1), 80 (hidden layer 2), 50 (hidden layer 3) and 30 (hidden layer 4). The model was trained with a number of different settings before arrivin at the final configuration. The accuracy of the trained model increasd to 74%, but test set accuracy was still around 73%. 

## Summary
While the accuracy of the model was still below expectation, there is no way to conclude if changing modeling design would improve performance or the data set was not comprehensive. However, in theory, retaining all the variables and not reducing dimensions should achieve 100% accuracy. However, that would defeat the purpose of modeling for prediction purpose. 
That said, it might be helpful to increase the number of hidden layers and neurons in each layer further to improve accuracy. However, there would be a trade-off in speed of execution and complexity of the model.




