
# Football Prediction

This is an exciting data science project that leverages machine learning algorithms to predict the outcome of football matches.

This project utilizes historical data from various football leagues and tournaments, including team performance, player statistics, and head-to-head records, to build models that can accurately predict the outcome of a football match. The project uses Python, Pandas, BeautifulSoup, requests, pickle, and scipy to process and predict data.

Overall, the Football Prediction project is a fascinating application of machine learning in the world of football. It not only provides valuable insights into the game but also enables users to make informed decisions that can enhance their enjoyment.


## Table Of Contents

- Prerequisites
- Installation
- Usage
- Contributions
- Conclusion
- License
- Related

## Prerequisites

- [Python (version 3.6 or later)](https://www.python.org/)
- [pandas](https://pandas.pydata.org/)
- [BeautifulSoup](https://beautiful-soup-4.readthedocs.io/en/latest/#:~:text=Beautiful%20Soup%20is%20a%20Python,hours%20or%20days%20of%20work.)
- [requests](https://pypi.org/project/requests/)
- [pickle](https://docs.python.org/3/library/pickle.html)
- [scipy](https://scipy.org/)
## Installation

- Clone the repository to your local machine
- Install the necessary libraries by running **`pip install -r requirements.txt`** in your terminal
    
## Usage

### Data Scraping

The data scraping process is done using the libraries pandas and beautifulsoup4.

1. #### **`scrape_group_tables.py`**

This script scrapes the group tables of the 2022 FIFA World Cup from Wikipedia and saves the tables as a dictionary in a pickle file named **`dict_table`**.

2. #### **`scrape_historical_data.py`**

This script scrapes the historical data of all FIFA World Cups from 1930 to 2018 from Wikipedia and saves the data as a CSV file named **`FIFA_World_Cup_Historical_Data.csv`**.

3. #### **`scrape_fixtures_data.py`**

This script scrapes the fixture data for the 2022 FIFA World Cup from Wikipedia and saves the data as a CSV file named **`FIFA_World_Cup_Fixtures_Data.csv`**.



### Data Cleaning and Analysis

The data cleaning and analysis is done using the libraries pandas, pickle, and scipy.


1. #### **`clean_historical_data.py`**

This script cleans the historical data of all FIFA World Cups from 1930 to 2018. It performs the following tasks:

- Deletes matches with walkover.
- Cleans blank spaces from HomeTeam, Score and AwayTeam columns.
- Splits score columns into Home and Away goals and drops the score column.
- Changes datatypes of HomeGoals, AwayGoals, and Year columns.
- Creates a new column **"TotalGoals"**.
- Saves the cleaned data as a CSV file named **`Clean_FIFA_World_Cup_Historical_Data.csv`**.


2. #### **`analyze_historical_data.py`**

This script analyzes the cleaned historical data of all FIFA World Cups from 1930 to 2018. It performs the following tasks:

- Calculates the average goals per match.
- Fits a Poisson distribution to the total goals data.
- Calculates the probability of a certain number of goals being scored in a match.
- Saves the probability data as a pickle file named **`probabilities.pickle`**.


3. #### **`predict_matches.py`**

This script predicts the results of the matches for the 2022 FIFA World Cup using the cleaned historical data and the Poisson distribution calculated in **`analyze_historical_data.py`**. It performs the following tasks:

- Loads the cleaned historical data and the Poisson distribution.
- Calculates the expected number of goals for each team in each match.
- Predicts the result of each match based on the expected number of goals.
- Saves the predicted results as a CSV file named **`Predicted_FIFA_World_Cup_Results.csv`**.

## Contribution

Contributions to this project are welcome. Please fork the repository and submit a pull request.
## Conclusion

This repository provides a comprehensive approach to scraping, cleaning, and analyzing FIFA World Cup data. It can be used to gain insights into the performance of teams, predict match outcomes, and understand the distribution of goals in FIFA World Cup matches.
## License

This project is licensed under the [MIT](https://choosealicense.com/licenses/mit/) License - see the LICENSE file for details.


## Related

Here are some related projects

- [Spotify_Analysis](https://github.com/RudraYug/Spotify_Analysis.git)

- [Tic_Tac_Toe](https://github.com/RudraYug/Tic_Tac_Toe.git)
