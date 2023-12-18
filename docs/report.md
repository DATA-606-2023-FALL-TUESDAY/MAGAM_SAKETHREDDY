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
   -  <a href="https://github.com/DATA-606-2023-FALL-TUESDAY/MAGAM_SAKETHREDDY/blob/main/data/saketh.pptx"><img src="https://img.shields.io/badge/-PowerPoint Presentation-B7472A?logo=microsoftpowerpoint&style=flat" alt="icon | GitHub"/></a>  
   - <a href="https://youtu.be/V5oO9iWJ-Bc"><img align="left" src="https://img.shields.io/badge/-YouTube-FF0000?logo=youtube&style=flat" alt="icon | YouTube"/></a> 
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
- To what extent can past match data, including team performance, and historical trends, inform predictions?
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
2. **Features/Predictors:**  `gf` (goals for), `ga` (goals against), `xg` (expected goals), `xga` (expected goals against), `poss` (possession)
- These features encompass a range of information related to the venue, opposition, timing, team performance, and other match characteristics, providing a comprehensive set of variables for your machine learning model in the football-related project.
3. **Machine Learning Models:**
- Random Forest
- Logistic Regression
- Support Vector Machine (SVM)
These models were selected to assess their performance in predicting Premier League match winners based on the provided features.
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
### 4.d Conversions
- Created a binary target variable indicating a win (1) or not (0) `matches["target"] = (matches["result"] == "W").astype("int")`

-  Converted categorical variables (venue and opponent) to numerical codes `matches["venue_code"] = matches["venue"].astype("category").cat.codes` `matches["opp_code"] = matches["opponent"].astype("category").cat.codes`

-  Extracted the hour from the "time" column and converted it to integer `matches["hour"] = matches["time"].str.replace(":.+", "", regex=True).astype("int")`

-  Converted the "date" column to datetime format `matches["date"] = pd.to_datetime(matches["date"])`

-  Extracted the day of the week and converted it to numerical code `matches["day_code"] = matches["date"].dt.dayofweek`
- `venue_code`, `opp_code`, `hour`, `day_code`, will be added to the features.
****


>## *_5. Model Training_*
### 5.a Machine Learning Models
- Random Forest (`RandomForestClassifier`)
- Logistic Regression (`LogisticRegression`)
- Support Vector Machine (SVM) (` SVC`)

### 5.b Training Procedures
- Employed an 80/20 train vs test split for model evaluation.
### 5.c Performance Metrics
- Accuracy
- Precision
- Recall
- F1-score

 ****
>## *_6. Model Results_*

### 6.a Metrics
After applying football-related data to various machine learning models, including Random Forest, Logistic Regression, and Support Vector Machine (SVM), the predictive outcomes were obtained. These models were trained to forecast Premier League match winners based on features like team performance, historical trends, and player statistics. The evaluation metrics, including accuracy, precision, recall, F1-score, and AUC-ROC, were calculated to assess the performance of each model. The results provide insights into the effectiveness of the machine learning models in predicting football match outcomes which have been provided below.

<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(13).png" alt="Premier League Logo" style="width: 700px; height: 200px;">
</p>

Following the execution of my football-related code through machine learning models, an observation revealed that the Random Forest model exhibited overfitting tendencies. Despite achieving high accuracy during training, the model struggled with generalization to new data, suggesting a need for further optimization and potential feature adjustments to address overfitting issues as presented below.
<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(17).png" alt="Premier League Logo" style="width: 700px; height: 200px;">
</p>

### 6.b Model Enhancement Strategies
1. Coefficient Interpretation
   -  In logistic regression, the coefficients represent the log-odds change in the probability of the dependent variable (target) being 1 for a one-unit increase in the corresponding independent variable, while holding other variables constant.
   -  Exponentiating these coefficients provides the odds ratio, indicating the proportional change in odds for the given variable.
<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(15).png" alt="Premier League Logo" style="width: 800px; height: 200px;">
</p>

<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(18).png" alt="Premier League Logo" style="width: 800px; height: 200px;">
</p>

2. Feature Importance
   - Assigned scores to input features based on their predictive utility.
   - Aided in model improvement and interpretation.
   - Utilizing the Random Forest model, feature importance analysis was conducted to discern the most influential factors affecting the predictions. 
   
<p align="center">
  <img src="https://github.com/saketh105/saketh105/blob/main/newplot%20(14).png" alt="Premier League Logo" style="width: 800px; height: 200px;">
</p>

*****
>## *_7. Research Queations Answered_*
1.Can historical match data accurately predict the outcomes of future Premier League matches?
- Depending on the complexity of factors influencing the game, while historical data provides valuable insights, the inherent unpredictability of football makes accurate predictions, and also has few challenges. 

2. To what extent can past match data, including team performance, and historical trends, inform predictions?
- Past match data, encompassing team performance, and historical trends, can offer substantial information for predictions. However, the prediction and feature importances show that these metrics have great impact.

3. Which machine learning algorithms and data features are most effective for match winner prediction in the Premier League?
- Machine learning algorithms such as Random Forest, Logistic Regression, and SVM, along with features like goals for (gf), goals against (ga), and expected goals (xg), prove effective for match winner prediction in the Premier League. 

4. Are there specific machine learning algorithms that outperform others in this context, and which features contribute significantly to prediction accuracy?
- Specific machine learning algorithms may outperform others based on the unique characteristics of the data. For instance, Random Forest excels at handling complexity, while Logistic Regression provides interpretability. The significance of features like goals for and against contributes significantly to prediction accuracy. However, random forest showed overfitting tendencies.

5. How can the predictive model be used to benefit football fans, sports analysts, and other stakeholders?
- The predictive model benefits football fans, sports analysts, and stakeholders by enhancing fan experience through informed insights into match outcomes. It provides a data-driven approach for understanding team performance and trends, aiding analysts in making informed predictions and supporting stakeholders in strategic decision-making.

6. In what ways can the model's predictions be applied to enhance the experience of Premier League enthusiasts, provide actionable insights, and support decision-making?
- The model's predictions can be applied to enhance the Premier League experience by providing enthusiasts with data-driven insights, facilitating informed betting decisions, and supporting sports analysts in creating engaging content. Additionally, stakeholders can use the predictions to optimize marketing strategies and sponsorship decisions based on anticipated match outcomes.
****
>## *_8. Conclusion_*
In conclusion, this project aimed to leverage historical football match data to predict Premier League outcomes using machine learning models. The exploration involved the application of Random Forest, Logistic Regression, and SVM, with a focus on features like team performance and historical trends. While Random Forest demonstrated exceptional accuracy, it also exhibited overfitting tendencies, highlighting the importance of model optimization.

The evaluation metrics, including accuracy, precision, recall, F1-score, and AUC-ROC, provided a comprehensive assessment of each model's performance. Logistic Regression, despite slightly lower accuracy, demonstrated robust precision, recall, and F1-score. On the other hand, SVM faced challenges in achieving satisfactory metrics.

The predictive model holds potential benefits for football enthusiasts, analysts, and stakeholders by offering data-driven insights into match outcomes. Despite the overfitting observed in the Random Forest model, this project serves as a foundation for further refinements and improvements. Future work could involve additional feature engineering, hyperparameter tuning, and the exploration of alternative models to enhance prediction accuracy and generalization. Overall, the project contributes valuable insights into the application of machine learning in football outcome predictions, laying the groundwork for continued research and refinement.
***
>## *_9. Future research_*
1. **Feature Engineering Exploration:** Delve into the identification of supplementary features or the derivation of novel ones, aiming to augment the models' predictive capabilities.

2. **Optimization of Hyperparameters:** Extend efforts in refining the hyperparameters of the machine learning models, striving for heightened generalization performance.

3. **Ensemble Methodology Investigation:** Explore the application of ensemble methods, amalgamating predictions from diverse models to potentially amplify overall accuracy and resilience.

4. **Temporal Analysis through Time-Series Techniques:** Consider the integration of time-series analysis techniques to capture temporal patterns and trends inherent in football performance data.

5. **Incorporation of Player-Specific Metrics:** Include metrics and statistics specific to individual players, providing insights into their distinct impact on match outcomes.

6. **Introduction of External Factors:** Integrate external factors like weather conditions, player injuries, or team dynamics, acknowledging their potential influence on match results.

7. **Exploration of Advanced Models:** Experiment with more sophisticated machine learning models or delve into deep learning architectures to unveil intricate patterns within the football dataset.

8. **Cross-League Prediction Scope:** Expand the prediction scope to encompass matches from diverse football leagues, evaluating the model's adaptability across different competitive landscapes.

These research pathways are poised to contribute to the refinement and fortification of predictive models, aligning with academic rigor and inquiry.
