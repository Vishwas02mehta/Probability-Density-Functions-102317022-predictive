# Probability-Density-Functions-102317022-predictive

Overview
This repository contains an academic project that demonstrates how to learn a probability density function (PDF) from real-world data using a roll-number-parameterized non-linear transformation and Maximum Likelihood Estimation (MLE). The implementation uses Python and is based on the India Air Quality dataset, focusing on the NO2 (Nitrogen Dioxide) feature.
Objectives
Apply a roll-number-based non-linear transformation to a dataset feature
Learn the parameters of a Gaussian probability density function
Estimate PDF parameters using Maximum Likelihood Estimation
Visualize the learned probability density function
Dataset
Dataset Name: India Air Quality Data
Source: Kaggle
Feature Used: no2
The dataset contains air quality measurements collected from multiple locations across India. In this project, only the NO2 column is used for analysis.
Methodology
Step 1: Non-Linear Transformation
Each NO2 value x is transformed into a new variable z using the following equation:
z = x + a_r * sin(b_r * x)

Where:
a_r = 0.05 * (r mod 7)
b_r = 0.3 * (r mod 5 + 1)
r = University Roll Number

This transformation introduces non-linearity and ensures that the model output is personalized for each roll number.

Step 2: Learning the Probability Density Function
The transformed variable z is modeled using a Gaussian probability density function:
p(z) = c * exp(-lambda * (z - mu)^2)

The parameters are estimated using Maximum Likelihood Estimation:

mu = mean(z)
sigma² = variance(z)
lambda = 1 / (2 * sigma²)
c = 1 / sqrt(2 * pi * sigma²)

Results
The code estimates the following parameters:
lambda (λ)
mu (μ)
c
A histogram of the transformed variable is plotted along with the learned Gaussian PDF to visually verify the fit.
Technologies Used
Python
NumPy
Pandas
Matplotlib
How to Run
Upload data.csv to Google Colab or your local Python environment
Update the roll number variable in the code
Run the script or notebook
Observe the estimated parameters and generated plot
Conclusion
The NO2 feature from the India Air Quality dataset was successfully transformed using a roll-number-based non-linear function. A Gaussian probability density function was learned using Maximum Likelihood Estimation. The estimated parameters define the learned PDF and demonstrate the application of statistical modeling techniques on real-world environmental data.
Author
Roll Number: 102317022
Project Type: Academic Assignment
Domain: Probability and Machine Learning
