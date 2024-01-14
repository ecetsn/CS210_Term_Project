# CS210_Term_Project: Sentiment Analysis through My WhatsApp Messages
This project involves sentiment analysis on WhatsApp messages, focusing on data collection, cleaning, and subsequent analysis to understand messaging habits and sentiment patterns throughout the day.

### Project Structure
1. Data Collection: WhatsApp messages are collected with timestamps.
2. Data Cleaning: Missing values are handled, text data is cleaned, and spell-checking is performed.
3. Message Intensity Analysis: The intensity of messages is observed over time and date periods.
4. Sentiment Analysis: The BERT-based Turkish model is used for sentiment analysis, and scores are calculated for each message.
5. Hypothesis Testing: Pearson correlation test is employed to assess correlations between sentiment scores during different time slots.
6. Habit Analysis: The total number of messages during different time slots is analyzed to derive messaging intensity ranks.

### Instructions
#### To reproduce the analysis:
- Install the necessary libraries mentioned in the notebook.
```shell
!pip install pandas
!pip install transformers
!pip install zemberek-nlp
!pip install plotly
!pip install seaborn
!pip install matplotlib
```
- Ensure the availability of WhatsApp data for analysis.
- Run the notebook in a Jupyter environment, following each step.

### Results
The analysis provides insights into messaging habits, sentiment patterns, and correlations between sentiment scores during various time slots. The report and .ipynb summarize key findings and interpretations.
