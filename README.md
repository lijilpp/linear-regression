# linear-regression
Pokémon Battle Outcome Prediction
A machine learning project that predicts the winner of Pokémon battles using regression analysis on combat data.
Overview
This notebook explores a dataset of 50,000 Pokémon battles and builds a Linear Regression model to predict which Pokémon will win a given matchup based on their IDs. The project covers data loading, exploratory analysis, model training, evaluation, and inference.
Dataset
combats.csv — 50,000 battle records with the following columns:
ColumnDescriptionFirst_pokemonID of the first Pokémon (1–800)Second_pokemonID of the second Pokémon (1–800)WinnerID of the winning Pokémon
Project Structure
Logistic_Regression.ipynb   # Main notebook
combats.csv                 # Battle dataset (upload manually)
README.md
Workflow

Import libraries — pandas, numpy, seaborn, matplotlib, scikit-learn
Load data — upload combats.csv via Google Colab file picker
Exploratory Data Analysis — inspect shape, head, and data types
Feature engineering — define features (First_pokemon, Second_pokemon) and target (Winner)
Train/test split — split data for model evaluation
Model training — fit a LinearRegression model from scikit-learn
Evaluation — compute R² score on both train and test sets
Prediction — predict the winner for a custom input pair

Results
SplitR² ScoreTrain0.3153Test0.3104
The R² of ~0.31 indicates that Pokémon ID alone is a weak predictor of battle outcomes. Incorporating actual stats (HP, Attack, Speed, etc.) from the Pokémon dataset would likely improve performance significantly.
Getting Started
Run on Google Colab (recommended)

Open the notebook in Google Colab
Run all cells in order
When prompted, upload combats.csv

Run locally
bashpip install pandas numpy seaborn matplotlib scikit-learn jupyter
jupyter notebook Logistic_Regression.ipynb

Note: Remove or replace the google.colab.files.upload() cell with a standard pd.read_csv('combats.csv') call when running locally.

Dependencies

Python 3.x
pandas
numpy
matplotlib
seaborn
scikit-learn

Possible Improvements

Merge with the Pokémon stats dataset to use attributes like HP, Attack, Defense, Speed, and Type as features
Try classification models (Logistic Regression, Random Forest, XGBoost) since the task is inherently binary (First wins vs Second wins)
Add feature engineering such as stat differentials between the two Pokémon
Perform hyperparameter tuning and cross-validation

License
This project is open source and available under the MIT License.
