# *_Project Title: Premier League Match Winners Prediction_*
<p align="center">
  <img src="https://github.com/saketh105/saketh/blob/main/Premier-League-logo.png" alt="Premier League Logo" style="width: 600px; height: 300px;">
</p>

****

> ## *_1. Author and resources_*
#### Author: Saketh Reddy Magam
#### Prepared for UMBC Data Science Master Degree Capstone under Dr Chaojie (Jay) Wang
   -  <a href="https://www.linkedin.com/in/saketh-reddy-magam-9b67bb161/"><img align="left" src="https://img.shields.io/badge/-LinkedIn-1E90FF?logo=linkedin&style=flat" alt="icon | LinkedIn"/></a>
   - <a href="https://github.com/saketh105"><img align="left" src="https://img.shields.io/badge/-GitHub-181717?logo=github&style=flat" alt="icon | GitHub"/></a>

#### Project Resources:
   -  <a href="https://github.com/DATA-606-2023-FALL-TUESDAY/MAGAM_SAKETHREDDY/edit/main/src/project_proposal.md"><img src="https://img.shields.io/badge/-PowerPoint Presentation-B7472A?logo=microsoftpowerpoint&style=flat" alt="icon | GitHub"/></a>  
   - <a href="https://youtube.com"><img align="left" src="https://img.shields.io/badge/-YouTube-FF0000?logo=youtube&style=flat" alt="icon | YouTube"/></a> 
****
> ## *_2. Project Focus_*

The project, _Premier League Match Winners Prediction_, centers around the development of a predictive model for forecasting the winners of matches in the Premier League, one of the most prestigious football (soccer) leagues globally. The primary aim is to leverage data analysis and machine learning techniques to make accurate match predictions.
### 2.a Significance:   
   1. **Enhanced Fan Experience:** Accurate match predictions enhance the fan experience by helping them decide which matches to watch, fostering engagement, and deepening their connection to the sport.
   2. **Data-Driven Insights:** The project provides valuable insights into team performance, player statistics, and trends, benefiting sports analysts and enthusiasts.
   3. **Betting and Gambling:** Match predictions are of interest to individuals involved in sports betting and gambling, as informed decisions can be made based on data-driven forecasts.

### 2.b Research Questions:
The following research questions guide the project
- Can historical match data accurately predict the outcomes of future Premier League matches?
- To what extent can past match data, including team performance, player statistics, and historical trends, inform predictions?
- Which machine learning algorithms and data features are most effective for match winner prediction in the Premier League?
- Are there specific machine learning algorithms that outperform others in this context, and which features contribute significantly to prediction accuracy?
- How can the predictive model be used to benefit football fans, sports analysts, and other stakeholders?
- In what ways can the model's predictions be applied to enhance the experience of Premier League enthusiasts, provide actionable insights, and support decision-making?
 
" _By addressing these research questions, the project aims to develop a robust and effective predictive model with practical applications and contribute to the understanding of match winner prediction in the context of the Premier League._"
****   
    
>## *_3. Data Description_*
   
### 3.a Data Sources:
The dataset for this project is collected from Football Reference Website, which includes Premier League official records,statistics, and historical football databases. It encompasses comprehensive information on Premier League matches, teams, players, and related statistics.
- website: [Football Reference](https://fbref.com/en/)

### 3.b Data Size:
The dataset consists of two files, one containing team statistics and the other containing shooting statistics that have been combined into a single file based on the individual components. However, as a reference:
- Total dataset size: Approximately 100KB
- Data Shape: The dataset is structured in tabular form, with multiple CSV (Comma-Separated Values) files representing different aspects of Premier League matches. The exact number of rows and columns *1598 rows and 27 coloumns*.

### 3.c Time Period:
The data cover a time span ranging from the inception of the Premier League in 2021 up to the most recent available season (2023-2024). Therefore, the dataset encompasses a time period spanning several seasons.

### 3.d Data Granularity: 
Each row in the dataset represents a single entity, with specific datasets focusing on different aspects:
- In the **_Stats_** dataset, each row represents a Premier League team. It includes team names, home stadiums, round, day, venue, result and other team-specific information.
- In the **_shooting_** dataset, each row represents an individual team shooting percentage and shooting specific statistics for the particular game.
- The **_Matches_** Dataset, it compromises of both these datasets.

### 3.e Data Dictionary:
**Matches Dataset Columns:**
| Column Name      | Data Type     | Definition                                              | Example Values                                  |
|------------------|---------------|---------------------------------------------------------|--------------------------------------------------|
| date             | datetime64    | The date on which the match was played.                 | '2022-01-15', '2022-02-03', etc.                |
| time             | object        | Time-related data for matches.                          | '15:30', '20:00', etc.                         |
| comp             | object        | The name of the competition or league.                  | 'Premier League', 'Champions League', etc.      |
| round            | object        | The round or stage of matches.                          | 'Matchweek 1' etc.             |
| day              | object        | The day of the week when matches occurred.              | 'Saturday', 'Wednesday', etc.                   |
| venue            | object        | The name of the venue or stadium where matches were played. | 'Home', 'Away', etc.              |
| result           | object        | The match result (e.g., "Win," "Loss," "Draw").         | 'Win', 'Loss', 'Draw'                          |
| gf              | float64       | The number of goals scored by the team (goals for).     | 2.0, 3.0, 1.0, etc.                            |
| ga              | float64       | The number of goals conceded by the team (goals against).| 0.0, 1.0, 2.0, etc.                            |
| opponent         | object        | The names of opponent teams.                            | 'Manchester City', 'Arsenal', etc.           |
| xg              | float64       | Expected goals scored by the team.                      | 1.5, 2.2, 0.8, etc.                             |
| xga             | float64       | Expected goals conceded by the team.                   | 1.0, 1.8, 0.5, etc.                             |
| poss            | float64       | Possession percentage for the team.                    | 55.2, 63.7, 48.9, etc.                         |
| attendance      | float64       | The number of attendees at the match.                  | 45000, 75000, etc.                             |
| captain          | object        | The captain of the team.                               | 'Harry Kane', 'Martin odegard', etc.             |
| formation        | object        | The team's formation used in the match.                | '4-3-3', '3-5-2', etc.                         |
| referee          | object        | The name of the match referee.                         | 'Michael Oliver', 'Felix Brych', etc.          |
| match report     | object        | Links or references to match reports.                  | na          |
| notes           | float64       | Additional notes or comments.                         | NaN, 1.0, 2.5, etc.                            |
| sh              | float64       | The number of shots taken by the team.                 | 15.0, 10.5, 8.0, etc.                          |
| sot             | float64       | The number of shots on target by the team.             | 7.0, 5.5, 3.0, etc.                            |
| dist            | float64       | Distance-related data (meaning may vary).              | 18.2, 25.5, 30.1, etc.                         |
| fk              | float64       | The number of free kicks awarded to the team.          | 12.0, 8.5, 15.0, etc.                          |
| pk              | float64       | The number of penalty kicks scored by the team.        | 2.0, 1.5, 0.0, etc.                            |
| pkatt           | float64       | The number of penalty kicks attempted by the team.     | 3.0, 2.5, 1.0, etc.                            |
| season           | int64         | The season or time period                             | 2022, 2023, etc.                     |
| team             | object        | The name of the team.                                  | 'Manchester United', 'Norwich City', etc.       |




_The data types may require further validation depending on the altercation of the dataset. Please note that columns with data type \"object\" typically contain strings or mixed data types, and may need to perform data type conversions or data cleaning as needed for analysis._
###Target and Features:
For our machine learning model, we will typically structure our dataset as follows:
1. **Target/Label:** The target variable will be a binary classification variable representing the match outcome (e.g., \"Home Team Win\" or \"Away Team Win\").
2. **Features/Predictors:** Potential features for our machine learning model may include Venue, opponent, time, date, various match-related statistics, performance indicators. The specific choice of features and target variable will be refined during the data preprocessing and model development stages of the project based on their relevance and performance in predicting match outcomes.
3. ** Machine Learning Models:** The Machine Learning Models will depend on the specific goals and tasks you want to accomplish with your data as we progress through the project.
***
>## *_4. Exploratory Data Analysis (EDA)_*
To comprehend the dataset thoroughly and lay the groundwork for subsequent model training, Exploratory Data Analysis (EDA) was conducted. Exploratory Data Analysis (EDA) is a crucial step to understand dataset characteristics. Employing Pandas, MatplotLib, and Plotly Visualizations, the initial exploration covered dataset shape, data types, and basic summary statistics. The exploration included data cleaning by addressing missing values and dropping unnecessary columns. Interactive Plotly visualizations provided insights into feature correlations and distributions. This multifaceted EDA set the stage for informed decisions in subsequent project stages.

### 4.a Preliminary Exploration with Pandas
Loaded the dataset from a CSV file located at the specified path `(C:\Users\13018\Downloads\matches.xls)`. The variable name assigned to this dataset is `matches`. 
- `matches.shape` - provides the number of rows and columns in the matches dataset.
- `matches.head()` - previewing the intial rows of the matches dataset.
- `matches.dtypes` - determining the data types for each column in the matches dataset.
- `matches.describe()` - provides key statistics for numerical columns, such as mean, standard deviation, and quartiles.
- `matches.info()` - information about the dataset, including data types and non-null counts.
- `neiss.isnull().sum()` - checking for the sum of missing values in each column, identifying areas that require cleaning.

### 4.b Data Cleaning
- The 'notes' column, found to be empty and unnecessary, is removed from the dataset.
- Additionally, missing values in the 'attendance' column are filled with the average attendance value.
- This series of steps ensures the dataset is prepared and free of missing values for subsequent analysis and modeling.

### 4.c Data Visualisation
Utilizing Plotly, the project explores dynamic and interactive visualizations to enhance the understanding of Premier League match winner predictions. The visualizations encompass diverse aspects, including team performance, historical trends, and key match statistics. Plotly enables the creation of informative charts and graphs that provide stakeholders with a comprehensive and engaging perspective on the data. This approach not only aids in uncovering patterns and insights but also facilitates effective communication of complex information, contributing to the overall success of the match winner prediction project.

#### 4.c.1 Stacked Bar chart for Goals Scored at Home vs. Goals Scored Away by Team 

<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(1).png" alt="Premier League Logo" style="width: 600px; height: 300px;">
</p>
Interpretation:
Each bar in the stacked bar chart represents a football team, with the lower red portion indicating goals scored at home and the upper light blue portion for goals scored away. The x-axis displays team names, and the y-axis shows the total goals (combined home and away). Text annotations at the bar tops show the number of games played. This visualization facilitates comparison of home and away goal distribution, assessment of team performance in different match venues, and understanding strengths and weaknesses of football teams.

#### 4.c.2 Sunburst chart for teams in different season based on the games won
<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(8).png" alt="Premier League Logo" style="width: 600px; height: 300px;">
</p>
Interpretation:
The sunburst chart hierarchically organizes data with outer rings representing seasons, inner rings for teams, and the final ring indicating goals scored. Each season segment is color-coded, and within it, team segments display the number of games won. Darker colors signify more wins. The size of each segment corresponds to the visualized value. This hierarchical visualization facilitates exploration of goals and wins by season and team. Selection of specific segments enables focused examination, and color-coded wins provide a rapid comparison of team performance across seasons.

#### 4.c.3 Violin Plot of Possession Distribution
<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(9).png" alt="Premier League Logo" style="width: 600px; height: 300px;">
</p>
Interpretation:
The violin plot visually represents possession distribution across teams, with each violin representing a team's spread and central tendency. Wider sections indicate higher data density, and the horizontal line within signifies the median possession value. The accompanying "box" provides quartile information. This visualization aids in comparing possession distributions among teams, with broader violins indicating greater variability. Teams with higher median lines exhibit elevated median possession values. The "box" succinctly summarizes possession quartiles for each team.

rest of the dat avisualisation can be found at .....

