# Sentiment Analysis through My WhatsApp Messages &middot; [![Build Status](https://img.shields.io/travis/npm/npm/latest.svg?style=flat-square)](https://travis-ci.org/npm/npm) [![npm](https://img.shields.io/npm/v/npm.svg?style=flat-square)](https://www.npmjs.com/package/npm) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/your/your-project/blob/master/LICENSE)
> The detailed results and steps are given in the .ipynb 

A project that conducts sentiment analysis on WhatsApp messages, exploring patterns and intensity of communication throughout the day.

## Installing / Getting Started

To get started, clone the project and navigate to the project directory. Install the required dependencies:

```shell
git clone https://github.com/ecetsn/CS210_Term_Project.git
cd CS210_Term_Project/
pip install -r requirements.txt
```

## Developing

## Built With
- Python
- Jupyter Notebook

## Prerequisites
- Python (>=3.6)
- Jupyter Notebook
- ZEMBEREK Turkish NLP library
- BERT-based Turkish sentiment analysis model
  
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

## Building
No additional building steps are required for this project.

## Deploying / Publishing
No specific deployment steps are needed as this project primarily focuses on analysis and exploration.

## Configuration
No user-configurable parameters. The configuration involves installing the required dependencies and setting up the environment.

## API Reference
No external API is used. The project primarily utilizes Python libraries for sentiment analysis and spell-checking.

## Steps for Analysis

### Sentiment Analysis
- Data Collection
  - Collecting conversational data from WhatsApp, ensuring the inclusion of timestamps for each interaction.
- Data Cleaning
   - Handle missing values
   - Convert to lowercase
   - Remove special characters
   - Remove links
   - Tokenization
   - Remove stopwords
   - Spell checking
     - Set the environment for Spell Checking using ZEMBEREK Turkish NLP
- Sentiment Analysis
  - Set the environment for Sentiment Analysis using BERT-based Turkish Mode 

### Habit Analysis
> After the data collection, the intensity of the conversation is observed according to time and date
- Get the intensity of messages
- Observe them by the periods of the day
- Combine this knowledge with the sentiment score of the messages

## Findings

### Sentiment Correlations Findings:

#### Analysis of Weighted Sentiment Over Time to Derive a Correlation Heatmap
In this analysis, I examine the trends in weighted sentiment over time by grouping the data based on date and time slots. The weighted sentiment is calculated and averaged for each group, resulting in a pivot table that provides insights into sentiment patterns during different times of the day.

![img5](https://github.com/ecetsn/CS210_Term_Project/assets/26511196/342872e4-f21f-44b8-a769-9de7f4d68a09)

#### Sentiment Scores Overview
In this analysis, a table containing sentiment scores for every message is presented. The sentiment scores were calculated using the BERT-Turkish model. This table serves as the foundation for hypothesis testing to explore patterns and trends in sentiment across different time slots.

![img2](https://github.com/ecetsn/CS210_Term_Project/assets/26511196/e5465bd3-7f57-424f-b895-a27bde3af8f0)

- The table provides a comprehensive view of sentiment scores for each message. These scores include both positive and negative values, allowing for a detailed examination of the sentiment distribution.

![img3](https://github.com/ecetsn/CS210_Term_Project/assets/26511196/f22cd989-a7f0-4a2e-ac41-f968b9f14693)

- The table provides a comprehensive view of positive sentiment scores for each message

![img4](https://github.com/ecetsn/CS210_Term_Project/assets/26511196/16f9bb70-f137-4aee-a93c-e72d18d34d3f)

- The table provides a comprehensive view of negative sentiment scores for each message

> These findings on sentiment correlation are used to test my hypothesis

## Hypothesis Testing
### Null Hypothesis(H0)
- There is no significant correlation between the selected periods of the day.
### Alternative Hypothesis(H1)
- There is a significant correlation between the selected periods of the day.

### Hypothesis Testing Technique:
- In this section, I employ the Pearson correlation test to assess the correlation between different variables.
The `pearsonr`  function is utilized to calculate both correlation coefficients and associated p-values for hypothesis testing.
#### Purpose:
- The Pearson correlation test is employed to understand the strength and direction of the linear relationship between two variables. This analysis provides insight into whether changes in one variable are associated with systematic changes in another.
#### Method:
- The code snippet utilizes the `pearsonr` function from the `scipy.stats` library to conduct hypothesis testing based on the Pearson correlation coefficient. This coefficient is employed to measure the linear relationship between two variables, providing insights into the strength and direction of their association. The accompanying p-value assists in evaluating the statistical significance of the observed correlation.

- In this context, the null hypothesis posits that there is no correlation between the specified pairs of variables. The code then calculates the p-value associated with the correlation coefficients for morning vs. night average sentiment and evening vs. noon average sentiment. The significance level (alpha) is set to 0.05, a commonly used threshold in hypothesis testing.

- The subsequent evaluation of results involves comparing the computed p-values with the chosen significance level. If a p-value is less than the significance level, it suggests that there is a statistically significant correlation between the respective pairs of variables. Conversely, if the p-value exceeds the significance level, the conclusion is that there is no significant correlation.

#### Morning vs. Night Sentiment:
- There is no significant correlation between morning average sentiment and night average sentiment.
#### Morning vs. Evening Sentiment:
- There is no significant correlation between morning average sentiment and evening average sentiment.
#### Morning vs. Noon Sentiment:
- There is no significant correlation between morning average sentiment and noon average sentiment.
#### Night vs. Evening Sentiment:
- There is no significant correlation between night average sentiment and evening average sentiment.
#### Night vs. Noon Sentiment:
- There is no significant correlation between night average sentiment and noon average sentiment.
#### Evening vs. Noon Sentiment:
- There is a **significant** correlation between evening average sentiment and noon average sentiment.

### Interpretation:
The lack of significant correlations in most comparisons suggests that the sentiment during one-time slot is generally independent of the sentiment during other time slots. This indicates that factors influencing sentiment may vary throughout the day. However, the significant correlation between evening and noon sentiment implies a potential pattern or similarity in sentiment during these specific time slots. Further investigation into the nature of this correlation may provide valuable insights into factors influencing sentiment during these times. This analysis lays the groundwork for understanding the temporal dynamics of sentiment and can guide future explorations or targeted interventions during specific time slots.

### Habit Analysis Findings:

![newplot](https://github.com/ecetsn/CS210_Term_Project/assets/26511196/5f0f56ea-6217-4706-8999-2a74b0df53bb)

![img1](https://github.com/ecetsn/CS210_Term_Project/assets/26511196/c406a4e0-950f-4a75-b748-212f3f570f9d)

The total number of messages during different time slots follows the following ranks:

#### Noon:
- Noon has the highest total number of messages, indicating that this time slot is the most active in terms of messaging intensity.
#### Evening:
- The evening comes next in terms of total messages, suggesting a considerable level of communication during this period.
#### Night:
- Nighttime exhibits a lower but significant total number of messages, signifying a notable level of activity during nighttime hours.
#### Morning:
- Morning shows the lowest total number of messages among the time slots, indicating relatively lower messaging activity during the morning hours.

#### Interpretation:
The observed ranks in messaging intensity provide valuable insights into my messaging habits. The highest activity during noon and evening may be influenced by various factors such as work schedules, social interactions, or personal preferences. The lower messaging intensity in the morning could be attributed to factors like work commitments or the start of the day.

> Understanding these patterns can help me manage my communication effectively and adapt to the natural rhythm of my messaging behaviour throughout the day.


## Licensing
This project is licensed under the MIT License. For details, refer to the LICENSE file.
