# Forecasting Premier League Goals Using Statistical and Machine Learning Models

## Overview
This project analyses Premier League match data to model and predict the number of goals scored by teams, using both econometric and machine learning approaches. A poisson regression framework is used to estimate the effects of team attack strength, opponent defence strength, and home advantage. A logsitic regression is also used to reframe the problem as a match outcome prediction. The project aims to compare interpretability and predictive performance across modelling approaches.

## Research Question
How many goals will a Premier League team score in a given match, and how does a structural statistical models compare to a machine learning classifier when forecasting match outcomes?

## Data
The analysis uses publicly available Premier League match data from the 2024/25 season. Each match is represented at both match and team level, with variables including  goals scores, home advantage, and team identities. 

## Methodology
## Exploratory data analysis
Goal distributions and scoring patterns analysed to motivate the use of count models.

## Poisson regression for goal modelling
Goals scored are modellie dusing a Poisson generalised linear model. The model includes team-specific attack effects, opponent defence effects, and a home advantage indicator. Coefficients are interpreted as multiplicative effects on expected goals.

## Comparison with a simple machine learning win classifier
Expected-goals estimates from the Poisson model are summarised into a single expected-goals difference feature. A logistic regression classifier is then trained on this difference to predict match outcomes (home win vs not home win), providing a machine learning benchmark on predictive accuracy.

## Results and Discussion
The Poisson model improves upon a naive basline when forecasting goals and provides interpretable estimates of team strengths (attack and defence) and home advantage. The logistic regression achieves reasonable classification accuracy for match outcomes, but sacrifices structural interpretability by relying on a compact feature representation that compresses multiple scoring mechanisms into a single expected-goals difference. This highlights the trade-off between explanation and prediction in sports analytics.

## Limitations and Extensions
All evaluations are in-sample and focus on binary outcomes. Future work could include out-of-sample validation, win-draw-loss classification, and the inclusion of richer match-level features.

## Tools
- Python
- pandas, numpy
- statsmodels
- scikit-learn
- matplotlib

## Status
Core modelling complete; further extensions possible.
