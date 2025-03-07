## 📋 Overview

This project develops a predictive model to estimate IMDb ratings for upcoming blockbuster films based on pre-release data. By analyzing approximately 2,000 previous movies, we identified key factors that influence public reception and created a robust polynomial regression model capable of accurately predicting movie ratings.

## 🎯 Project Goals

- Predict IMDb ratings for upcoming blockbuster films using pre-release characteristics
- Identify the most significant variables that influence movie ratings
- Develop a robust model that minimizes bias, heteroskedasticity, and overfitting
- Provide insights to stakeholders in the film industry for informed decision-making

## 📊 Dataset

The dataset contains information on 1,930 films with 41 independent variables including:
- Movie characteristics (budget, duration, genre, maturity rating)
- Cast details (actor star meter rankings)
- Production information (director, cinematographer, distributor)
- Media coverage (number of news articles)
- Platform metrics (IMDbPro movie meter)

## 🔍 Methodology

### Data Preprocessing

- Excluded irrelevant label variables (movie_title, movie_id, imdb_link)
- Removed variables with limited predictive power (release_day, release_month, release_year)
- Removed redundant or irrelevant features (plot_keywords, colour_film, language)
- Addressed skewed distributions via log transformation
- Managed outliers by removing values above the third quartile
- Recategorized genres and personnel for more effective analysis

### Feature Engineering

- Applied log transformation to skewed numerical variables
- Consolidated low-frequency genres into an "other" category
- Created dummy variables for top performers in each personnel category
- Identified and managed multicollinearity among predictors

### Model Development

1. Performed simple linear regressions to identify significant predictors
2. Built multiple linear regression with numerical variables
3. Tested for collinearity using VIF scores
4. Addressed heteroskedasticity through log transformations
5. Added categorical variables to improve model performance
6. Implemented polynomial terms for non-linear variables
7. Finalized model with highest predictive power

## 🔑 Key Findings

The most significant predictors of IMDb ratings include:

**Positive Impact Variables:**
- Movie duration (non-linear relationship)
- Number of news articles
- IMDbPro movie meter
- Drama, War, Adventure, Crime, and Biography genres
- Top directors, cinematographers, and distributors

**Negative Impact Variables:**
- Horror, Action, and Comedy genres
- USA production (suggesting higher expectations)
- Actor star power (complex non-linear relationship)

## 📈 Results

Our final model achieved:
- R-squared: 0.4857
- Adjusted R-squared: 0.476
- MSE: 0.5967

## 💡 Insights

- Budget significantly impacts rating expectations, with higher budgets correlating with higher ratings
- Media coverage plays a crucial role in rating predictions
- Drama and biography genres typically receive higher ratings
- Horror and comedy genres generally receive lower ratings
- R-rated movies typically score higher than PG-rated films
- Production team quality (directors, cinematographers, distributors) significantly influences ratings

## 📚 Future Work

- Incorporate NLP techniques to analyze movie descriptions and plot summaries
- Develop more sophisticated ensemble models to improve predictive accuracy
- Include additional external factors such as competition in release window
- Create a web application for real-time prediction of upcoming movie ratings

## 👥 Contributors

- Xinyi Wang
- JaeYoon Lee
- Yifei Liu
- Jintao Li
- Shuxi Chen
