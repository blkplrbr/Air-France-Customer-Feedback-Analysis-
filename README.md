# Air-France-Customer-Feedback-Analysis-
Data came from Kaggle. project focused on cleaning, standardization , and formula based text analysis to transform raw, unstructures customer reviews into actionable insights
## Data cleaning process:
  * Data linking :used data linking formula ot copy over information from the raw data set and clean without harming source data integrity. 
  * text cleaning :applied trim lower nested formula to conevert all review text into lower case and remove excess spacing. 
  * punctuation removal : used nested substitute functions to remove pnctuation 
  * sentiment analysis : Created a sentiment column using if /is number /search formula to tag reviews as positive, negative or neutral based on key phrases (eg: "great", "bad", "terrible"). 
  *data quality* : verified cleaned state of data . no blankrows or columns. 

  ## Key findings: 
  * total volume of feedback (pivot table):
    * total count of ratings is 2560
    *  count of rated 1 is 25.19%
    *  count of rated 5 is 25.43%
  * Overall Sentiment Findings (pivot table) :
    *   total volume of sentiments is 2331
    *   largest count is neutral at 2331 ( 91 %)
    *   smallest count is negative at 52 (2.03 %)
  * Sentiment vs Rating Comparison (pivot table ):
    * tested sentiment analysis agaisnt ratings to understand what more could be leanred. method is not picking up any anamalies ( read : high numbers of negative sentiment but rated as rating 5.) mot sentiment is found neutral and the spread seems mostly even between 1-5 with the heavier weight put towards neutral -4,5. 
