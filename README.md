# KingHouse_prediction-372
## Project Goal
The King County House Dataset contains a wealth of information about the price, size, location, condition and various other features of houses in Washington’s King County. In this article, I’ll present how I built a multiple linear regression model in Python to predict house prices.</.

## Findings
My current preferred model is able to explain about 58% of the variance in the sale prices of homes, and on average predicts a sale price that is 145,000 away from the actual sale price

## Data Source and Data Exploration
This data comes from a Kaggle competition which provides details about homes in King County housing.

The target variable shows that there are some outliers in the data, which are homes that were sold at much higher prices than most of the other homes in the dataset.

I used 13 columns for my analysis, which included variables about:

the zipcoge,longitude and Latitudes
the total size of both the lot and the house itself
the number of bedrooms and bathrooms
additional features like views, waterfront basements, etc.
The most correlated feature to the price is sqft_living, which was also the most informative feature in my preferred model, is the Overall Quality of the house (OverallQual).

## Data Preparation
II dropped the Id, date and sqft_ basement column since we wont be using it and has null values
The watefront column had missing values so we replaced with the mode which was none
The view column had missing values so we filled with the mode which was No

## Modeling
I began with a OSL that predicts only the mean house price from the training data for each house. My final model is QQ plot It compares the quantiles of the residuals to the quantiles of a theoretical normal distribution

model_comparison3

Evaluation
I used both the Coefficient of Determination (R2 Score) and Mean Absolute Error to evaluate my models. I wanted to make sure these two very different metrics were evaluated so I could see how my models are trending overall. The benefit of R2 Score is I can see how well my model explains the variance of the target, the house sale price, while the Mean Absolute Error is able to explain how off my predictions were on average in real dollar terms. I trained my model on two-thirds of the data for which I knew the actual sale price, then tested my results on the remaining third.

Conclusion
Nearly all of the model coefficients have p-values less than 0.05 and are thus statistically significant.
The bathroom variables does help predict prices
Our model has 58% variance in price which shows an improvement from our previous model
The more the variables the higher the significance/Accuracy level
For every increase in 1 squarefoot living in 15 neighbourhoods, the price of the house increases by 99.703009dollars
Mean Absolute error is 145001 meaning that there is a difference of 145001 between the actual price and our predicted price: * Our MAE has reduced showing that the more you add independent variables the more accurate your prediction will be

### Repository Guide
├── code                                       Code folder, data cleaning and visualization functions
├── data                                       Data folder, which is not included in this repository
                                    
├── Student.ipynb              Main Jupyter notebook, contains analysis
├── King_House Tableau.pdf    PDF Version of Tableau dashboard

├── README.md                                  The top-level README 
└── __init__.py                                python package file

## Reproduction Instructions
This project uses:

Anaconda, a package and environment management tool

Python 3.6.9, with the following additional packages/libraries:

Pandas 0.25.1
NumPy 1.16.5
Matplotlib 3.1.1
Seaborn 0.9.0
Scikit-Learn 0.22.1

If you would like follow the analysis locally and have the above tools:

Fork and clone this repository
Go to the Kaggle competition page and download the data files
Save the train.csv data file into a data/ folder which is at the same level as the notebook
You should then be able to run the exploration and analysis in the provided EDA-Modeling-Evaluation Jupyter Notebook.

### Sources:
Data Source: Kaggle
README Header Image Source: Lending Tree
### Contact Information
With questions or feedback on this repository, please reach out via:

GitHub
LinkedIn
