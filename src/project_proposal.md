# *_Project Title: Premier League Match Winners Prediction_*
![Premier-League-logo.png](https://github.com/saketh105/saketh/blob/main/Premier-League-logo.png)
## *Prepared for UMBC Data Science Master Degree Capstone under Dr Chaojie (Jay) Wang*
### Author: Saketh Reddy Magam
   - [GitHub Profile](https://github.com/saketh105)
   - [LinkedIn Profile](https://www.linkedin.com/feed/)

### Project Resources:
   - [PowerPoint Presentation](link-to-your-ppt-presentation.pdf)
   - [YouTube Video](link-to-your-youtube-video)

> ## *_Project Focus_*

The project, _Premier League Match Winners Prediction_, centers around the development of a predictive model for forecasting the winners of matches in the Premier League, one of the most prestigious football (soccer) leagues globally. The primary aim is to leverage data analysis and machine learning techniques to make accurate match predictions.
### Significance:   
   1. **Enhanced Fan Experience:** Accurate match predictions enhance the fan experience by helping them decide which matches to watch, fostering engagement, and deepening their connection to the sport.
   2. **Data-Driven Insights:** The project provides valuable insights into team performance, player statistics, and trends, benefiting sports analysts and enthusiasts.
   3. **Betting and Gambling:** Match predictions are of interest to individuals involved in sports betting and gambling, as informed decisions can be made based on data-driven forecasts.

### Research Questions:
The following research questions guide the project
- Can historical match data accurately predict the outcomes of future Premier League matches?
- To what extent can past match data, including team performance, player statistics, and historical trends, inform predictions?
- Which machine learning algorithms and data features are most effective for match winner prediction in the Premier League?
- Are there specific machine learning algorithms that outperform others in this context, and which features contribute significantly to prediction accuracy?
- How can the predictive model be used to benefit football fans, sports analysts, and other stakeholders?
- In what ways can the model's predictions be applied to enhance the experience of Premier League enthusiasts, provide actionable insights, and support decision-making?
 
" _By addressing these research questions, the project aims to develop a robust and effective predictive model with practical applications and contribute to the understanding of match winner prediction in the context of the Premier League._"
****   
    
>## *_Data Description_*
   
### Data Sources:
The dataset for this project is collected from Football Reference Website, which includes Premier League official records,statistics, and historical football databases. It encompasses comprehensive information on Premier League matches, teams, players, and related statistics.
- website: [Football Reference](https://fbref.com/en/)

### Data Size:
The dataset consists of two files, one containing team statistics and the other containing shooting statistics that have been combined into a single file based on the individual components. However, as a reference:
- Total dataset size: Approximately 100KB
- Data Shape: The dataset is structured in tabular form, with multiple CSV (Comma-Separated Values) files representing different aspects of Premier League matches. The exact number of rows and columns 1598 rows and 27 coloumns.

### Time Period:
The data cover a time span ranging from the inception of the Premier League in 2021 up to the most recent available season (2023-2024). Therefore, the dataset encompasses a time period spanning several seasons.

### Data Granularity: 
Each row in the dataset represents a single entity, with specific datasets focusing on different aspects:
- In the **_Stats_** dataset, each row represents a Premier League team. It includes team names, home stadiums, round, day, venue, result and other team-specific information.
- In the **_shooting_** dataset, each row represents an individual team shooting percentage and shooting specific statistics for the particular game.
- The **_Matches_** Dataset, it compromises of both these datasets.

### Data Dictionary:
**Matches Dataset Columns:**

- date (object): The date on which the match was played.
- time (object): Time-related data for matches.
- comp (object): The name of the competition or league.
- round (object): The round or stage of matches.
- day (object): The day of the week when matches occurred.
- venue (object): The name of the venue or stadium where matches were played.
- result (object): The match result (e.g., \"Win,\" \"Loss,\" \"Draw\").
- gf (object): The number of goals scored by the team (goals for).
- ga (object): The number of goals conceded by the team (goals against).
- opponent (object): The names of opponent teams.
- xg (float64): Expected goals scored by the team.
- xga (float64): Expected goals conceded by the team.
- poss (float64): Possession percentage for the team.
- attendance (float64): The number of attendees at the match.
- captain (object): The captain of the team.
- formation (object): The team's formation used in the match.
- referee (object): The name of the match referee.
- match report (object): Links or references to match reports.
- notes (object): Additional notes or comments.
- sh (float64): The number of shots taken by the team.
- sot (float64): The number of shots on target by the team.
- dist (float64): Distance-related data (meaning may vary).
- fk (float64): The number of free kicks awarded to the team.
- pk (float64): The number of penalty kicks scored by the team.
- pkatt (float64): The number of penalty kicks attempted by the team.
- season (int64): The season or time period (assuming it should be of integer data type).
- team (object): The name of the team.

_The data types are based on the information provided and may require further validation depending on the actual content of the dataset. Please note that columns with data type \"object\" typically contain strings or mixed data types, and you may need to perform data type conversions or data cleaning as needed for analysis._
***
>## _Target and Features_

For our machine learning model, we will typically structure our dataset as follows:
1. **Target/Label:** The target variable will be a binary classification variable representing the match outcome (e.g., \"Home Team Win\" or \"Away Team Win\").
2. **Features/Predictors:** Potential features for our machine learning model may include Venue, opponent, time, date, various match-related statistics, performance indicators. The specific choice of features and target variable will be refined during the data preprocessing and model development stages of the project based on their relevance and performance in predicting match outcomes.
3. ** Machine Learning Models:** The Machine Learning Models will depend on the specific goals and tasks you want to accomplish with your data as we progress through the project.

  
