**Football Shot Analysis Project**

**Overview:**
This project analyzes football shot data to evaluate team and positional performance across major competitions, including the Premier League, La Liga, Ligue 1, Champions League, FIFA World Cup, and Women's World Cup. The dataset, football.csv, contains detailed shot information such as expected goals (xG), shot distance, shot angle, and defensive density. The project processes this data to derive insights into team performance metrics and positional contributions, focusing on expected goals and actual goals scored.

**Objectives:**
Data Cleaning and Filtering: Filter the dataset to focus on specific competitions and seasons, and preprocess shot types to include only "Open Play" and "Free Kick" shots.
Team Performance Analysis: Compute team-level statistics, including total shots, goals, expected goals (xG), and advanced metrics like Advance_xG and Advance_LxG.
Positional Analysis: Evaluate the contribution of different player positions (defender, midfielder, attacker) in terms of expected and actual goals in specific competitions.
Exploratory Data Analysis: Summarize numerical and categorical features to understand shot characteristics and their distribution.

**Dataset:**
The dataset (football.csv) contains 82,821 shot records with 25 features, including:
Numerical Features: stats_xg, shot_distance, shot_angle, defence_density, x_list, y_list
Categorical Features: competition_name, season_name, shot_type, shot_outcome, position_name, team_name, etc.

**Key Metrics:**
stats_xg: Expected goals for each shot.
shot_outcome: Whether the shot resulted in a goal ("Goal" or "No Goal").
Advance_xG and Advance_LxG: Advanced expected goal metrics for enhanced analysis.

**Methodology:**
**Data Preprocessing**: Loaded the dataset using pandas and inspected its structure with .info() and .describe().
The dataset was filtered to include only relevant competitions and seasons. Unnecessary columns were dropped and categorical features were cleaned and consolidated. For example, player positions were grouped into broader categories like 'attacker', 'midfielder' and 'defender'
Filtered data to include only major competitions: Premier League, La Liga, Ligue 1, Champions League, FIFA World Cup, and Women's World Cup.
Restricted seasons to a specific range (2010/2011 to 2022/2023).
Included only "Open Play" and "Free Kick" shot types to focus on common scenarios.
Handled missing values and ensured data consistency.

**Feature Engineering:** New features were created from the existing data to better capture the context of each shot. This included categorizing player positions and shot types.

**Exploratory Data Analysis (EDA):** The cleaned data was analyzed to understand the relationships between different variables and the likelihood of a goal. This included visualizing the distribution of numerical features and the correlation between variables.

**Model Building and Evaluation:** Several machine learning models were built and evaluated to predict the outcome of a shot. These included Logistic Regression, Random Forest, Decision Tree, and XGBoost classifiers. The models were trained on a portion of the data and evaluated on a separate test set to assess their performance.

**Model Interpretation:** SHAP (SHapley Additive exPlanations) analysis was used to understand the predictions of the best-performing model. This technique helps to explain how each feature contributes to the model's output, providing insights into the factors that are most important for predicting a goal.

**Team Statistics:**
Implemented the team_stats function to calculate:
Total shots and goals per team.
Expected goals (stats_xg), shot quality and goal-to-shot ratios.
Advanced metrics (Advance_xG, Advance_LxG) for deeper insights.
Ratios comparing stats_xg to advanced metrics.
Generated team performance tables for the Premier League and Champions League.

**Positional Statistics:**
Developed the pos_stats function to analyze contributions by player position (defender, midfielder, attacker) in a given competition.
Calculated total Advance_xG, Advance_LxG, stats_xg, and actual goals for each position.

**Dependencies:**
Python libraries: pandas, numpy, sklearn, xgboost, shap, matplotlib.
Used for data manipulation, machine learning, feature importance analysis, and visualization.

**Key Findings:**
Team Performance:
Shot Distance and Angle: As expected, the distance and angle of a shot are highly correlated with the probability of scoring. Closer shots from a more central position have a much higher chance of being successful.
Defensive Pressure: The presence of defensive pressure significantly reduces the likelihood of a goal.
Shot Type and Technique: Different shot types and techniques have varying success rates. For example, a volley from close range may be more likely to score than a long-range shot from a free kick.
In the Premier League, Manchester City led with 606 shots and 66 goals, with a high stats_xg of 58.29, indicating strong attacking efficiency.
In the Champions League, Real Madrid topped with 77 shots and 11 goals, with a stats_xg of 7.66, showing clinical finishing (Goals to stats_xg ratio: 1.44).
Teams like Tottenham Hotspur and Bayern Munich showed varying efficiencies, with Tottenham underperforming relative to their stats_xg in the Champions League.











