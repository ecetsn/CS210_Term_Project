# Sentiment Analysis through My WhatsApp Messages &middot; [![Build Status](https://img.shields.io/travis/npm/npm/latest.svg?style=flat-square)](https://travis-ci.org/npm/npm) [![npm](https://img.shields.io/npm/v/npm.svg?style=flat-square)](https://www.npmjs.com/package/npm) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/your/your-project/blob/master/LICENSE)

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
