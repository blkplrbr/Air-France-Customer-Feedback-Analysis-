# Air France Customer Feedback Analysis

## Project Overview
This project focused on cleaning, standardizing, and performing formula-based text analysis on raw, unstructured customer reviews (sourced via Kaggle) to transform them into actionable business insights. 

## Data Cleaning & Preparation Process
To ensure data integrity, a strict cleaning SOP was established before analysis:

*   **Data Linking:** Utilized data linking formulas to duplicate and clean information from the raw dataset without harming the integrity of the source data.
*   **Text Standardization:** Applied nested `TRIM` and `LOWER` functions to convert all review text into lowercase and remove excess spacing.
*   **Punctuation Removal:** Utilized nested `SUBSTITUTE` functions to strip punctuation from the text strings.
*   **Sentiment Tagging:** Created a custom sentiment column using nested `IF` / `ISNUMBER` / `SEARCH` formulas to automatically tag reviews as positive, negative, or neutral based on keyword triggers (e.g., "great", "bad", "terrible"). 
*   **Data Quality Check:** Verified the cleaned state of the data, ensuring no blank rows or columns remained.

## Key Findings
Through the use of Pivot Tables, several key insights were discovered:

*   **Total Volume of Feedback:**
    *   Total count of ratings: **2,560**
    *   Count of 1-star ratings: **25.19%**
    *   Count of 5-star ratings: **25.43%**
*   **Overall Sentiment Findings:**
    *   Total volume of tagged sentiments: **2,331**
    *   Largest count was **Neutral at 91%**
    *   Smallest count was **Negative at 2.03%**
*   **Sentiment vs. Rating Comparison (The Anomaly):**
    *   Tested the formula-based sentiment analysis against the numerical ratings to see what more could be learned. 
    *   **The Result:** The keyword method was not picking up on anomalies (e.g., high numbers of negative sentiment paired with a 5-star rating). Furthermore, the overall sentiment was heavily skewed toward "Neutral" (spread mostly evenly between 1-5), indicating that basic keyword searches are insufficient for capturing the nuance of customer feedback. 

## Next Steps (The Python Pivot)
Because the basic Excel keyword formula resulted in a 91% "neutral" catch-all and missed contextual anomalies, this project demonstrates the exact limitations of Excel-based text analysis. The logical next step (documented in my Python portfolio) is to transition this dataset into Python/Pandas to utilize advanced NLP libraries (like VADER or TextBlob) for more accurate contextual sentiment analysis.
