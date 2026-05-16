# steam-games-success-analysis
• R-based statistical analysis of paid Steam games using Kaggle's Steam Games Dataset 2025, focusing on reviews, price, genre, playtime, and multiplayer features.
• This was my Introduction to Probability and Statics final project

# Goal
• The main goal of this project was to determine which variables best predict or relate to the commercial success of paid Steam games.
• Our composite success metric defined as the product of total review count and price

# Dataset
• Dataset used in this project was the Steam Games Dataset 2025  from Kaggle https://www.kaggle.com/datasets/artermiloff/steam-games-dataset
• For this analysis, We restricted our daset into:
• Metacritic score > 0 
• Price > 0
• Median playtime > 0 
• Average playtime > 0
• After filtering the data, our sample included 1,557 paid games

# Research Questions
Q1. Is the Metacritic critic score or the Steam user-review percentage a better single predictor of success?
Q2. Does combining both scores meaningfully improve prediction over the better single predictor?
Q3. Are some genres systematically associated with higher success after controlling for other genre tags?
Q4. Is higher price positively correlated with success?
Q5. Is median playtime or average playtime the better predictor of success?
Q6. Do multiplayer games achieve higher success than single-player games?
Q7. Is price efficiency (median hours per dollar) associated with success?

# Variables Used
• metacritic_score: critic score of the game
• pct_pos_total: percentage of positive Steam user reviews
• price: price of the game
• num_reviews_total: total number of user reviews
• median_playtime_forever: median playtime in minutes
• average_playtime_forever: average playtime in minutes
• genres: genre tags for each game
• categories: category tags used to identify multiplayer gamese used 

# Derived Variables
• success_score = num_reviews_total * price
• log_success: logged version of success score
• price_efficiency = median_playtime_forever / price
• log_price_efficiency: logged version of price efficiency
• log_num_reviews: logged version of total reviews
• player_mode: multiplayer or single-player classification
• Genre indicator variables for Action, Adventure, Casual, Indie, RPG, Simulation, Strategy, Sports, and Racing

# Methods
• All analysis was conducted in R using tidyverse, dplyr, ggplot2, broom and some R statistical functions
• We used: 
• Data cleaning and filtering
• Exploratory data visualization
• Simple linear regression
• Multiple linear regression
• Regression diagnostics
• Welch two-sample t-test
• Spearman correlation

# Findings
• Metacritic critic score was a stronger single predictor of success than Steam user-review percentage.
• Combining Metacritic score and Steam user-review percentage improved prediction, but only modestly.
• Simulation, Action, and RPG games were associated with higher success after controlling for overlapping genre tags.
• Indie-labeled games were associated with lower success after controlling for other genre tags.
• Higher-priced games were positively correlated with success, although this should be interpreted carefully because price is part of the success score formula.
• Average playtime was a better predictor of success than median playtime.
• Multiplayer games had higher average log success scores than single-player games.
• Price efficiency had little meaningful relationship with success.

# Limitations
• Tautological price effect
• Selection bias
• Cannot detect nonlinearity or price ceilings
• Single time-point snapshot

# Files
• steam_games_analysis.Rmd: R Markdown file containing the analysis code
• final_project_paper.pdf: final written project report
• README.md: information about the project

# Reproduce the Analysis
• Download the Steam Games Dataset 2025 from Kaggle
• Placed the cleaned CSV file in a folder
• Name the file: games_march2025_cleaned.csv
• Open steam_games_analysis.Rmd in RStudio
• Run the file

# Skills Demonstrated
• R programming
• Data cleaning
• Data visualization
• Regression modeling
• Hypothesis testing
• Statistical interpretation
• Working with real-world data
• Communicating results through a written report

# Contributors
• Mikey Pole
• Augie Jones
• Luis Jiang
