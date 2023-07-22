# ML-Medical-Insurance-Cost-Predictor

Dataset download: https://www.kaggle.com/datasets/mirichoi0218/insurance

# Insurance Cost Prediction using Linear Regression

This repository contains code to train a Linear Regression model for predicting insurance costs based on various features such as age, sex, BMI, number of children, smoking status, and region.

## Dependencies

Before running the code, ensure you have the following dependencies installed:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

You can install these dependencies using pip:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Data Collection and Processing

The code reads insurance data from a CSV file named "insurance.csv" and stores it in a Pandas DataFrame. The first five rows of the dataset are displayed using `insuranceDataSet.head()`. The dataset contains the following columns:

- age: Age of the insured
- sex: Gender of the insured (male or female)
- bmi: Body mass index of the insured
- children: Number of children covered by the insurance
- smoker: Smoking status of the insured (yes or no)
- region: Geographic region of the insured
- charges: Insurance charges

## Data Analysis

Several data analysis steps are performed to understand the dataset. These include:

- Checking for missing values (no missing values are found).
- Descriptive statistics of the numerical features (age, BMI, children, charges).
- Visualization of the distribution of age, sex, BMI, number of children, smoking status, region, and insurance charges.

## Data Pre-processing

Before training the model, the categorical features (sex, smoker, region) are encoded into numerical values for compatibility with the algorithm. The encoding is as follows:

- 'sex': 'male' is encoded as 0, 'female' is encoded as 1.
- 'smoker': 'yes' is encoded as 0, 'no' is encoded as 1.
- 'region': 'southeast' is encoded as 0, 'southwest' is encoded as 1, 'northeast' is encoded as 2, 'northwest' is encoded as 3.

## Model Training

The dataset is split into training and testing sets using the `train_test_split` function from scikit-learn. A Linear Regression model is trained using the training data.

## Model Evaluation

The model is evaluated on both the training and testing datasets using the R-squared value. The R-squared value measures how well the model fits the data, with values close to 1 indicating a good fit.

## Predicting Insurance Cost

A sample input data is provided in the form of a tuple (age, sex, BMI, children, smoker, region), and the trained model predicts the insurance cost based on this data.

## How to Use

To use this code, follow these steps:

1. Install the required dependencies as mentioned above.
2. Place the "insurance.csv" file containing the insurance dataset in the appropriate directory.
3. Run the code in your preferred Python environment.

Note: Ensure that the input data provided for predicting the insurance cost matches the format (age, sex, BMI, children, smoker, region) as described in the "Build a predicting system" section of the code.

Feel free to modify the code and explore different aspects of the dataset and model to gain further insights. Happy coding!
