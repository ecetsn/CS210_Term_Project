# Sentiment Analysis through My WhatsApp Messages &middot; [![Build Status](https://img.shields.io/travis/npm/npm/latest.svg?style=flat-square)](https://travis-ci.org/npm/npm) [![npm](https://img.shields.io/npm/v/npm.svg?style=flat-square)](https://www.npmjs.com/package/npm) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/your/your-project/blob/master/LICENSE)
> The detailed results and steps are given in the .ipynb 

A project that conducts sentiment analysis on WhatsApp messages, exploring patterns and intensity of communication throughout the day.

## Installing / Getting started

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

## Findings

### Sentiment Correlations Findings:
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
The lack of significant correlations in most comparisons suggests that the sentiment during one time slot is generally independent of the sentiment during other time slots. This indicates that factors influencing sentiment may vary throughout the day. However, the significant correlation between evening and noon sentiment implies a potential pattern or similarity in sentiment during these specific time slots. Further investigation into the nature of this correlation may provide valuable insights into factors influencing sentiment during these times. This analysis lays the groundwork for understanding the temporal dynamics of sentiment and can guide future explorations or targeted interventions during specific time slots.

### Habit Analysis Findings:
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

## Building
No additional building steps are required for this project.

## Deploying / Publishing
No specific deployment steps are needed as this project primarily focuses on analysis and exploration.

## Versioning
We use SemVer for versioning. For the versions available, see the link to tags on this repository.

## Configuration
No user-configurable parameters. The configuration involves installing the required dependencies and setting up the environment.

## Tests
Tests are not implemented for this project as it focuses on exploratory data analysis.

## Style guide
The code follows PEP 8 style guidelines. You can check it using tools like flake8.

## API Reference
No external API is used. The project primarily utilizes Python libraries for sentiment analysis and spell-checking.

## Database
No external database is used for this project. It mainly involves processing and analyzing text data.

## Licensing
This project is licensed under the MIT License. For details, refer to the LICENSE file.
