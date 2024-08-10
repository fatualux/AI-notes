# Logistic Regression

Logistic regression is a statistical method used for binary classification problems. It models the probability that a given input belongs to a particular class by applying a logistic function to a linear combination of the input features.

## Logistic Regression Formula

The logistic regression model predicts the probability of a binary outcome using the logistic function:

\\[ P(Y = 1 \mid X) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 X)}} \\]

where:

- **\( P(Y = 1 \mid X) \)**: Probability of the response variable \( Y \) being 1 given predictor variable \( X \).
- **\( \beta_0 \)**: Intercept term.
- **\( \beta_1 \)**: Coefficient for the predictor variable \( X \).
- **\( e \)**: Base of the natural logarithm (approximately 2.718).

### Table of Terms

| Formula                                    | Meaning                       | Interpretation                                                   |
|--------------------------------------------|-------------------------------|-------------------------------------------------------------------|
| \\( P(Y = 1 \mid X) \\)                    | **Probability**               | Probability of the positive class (Y = 1)                       |
| \\( \frac{1}{1 + e^{-(\beta_0 + \beta_1 X)}} \\) | **Logistic Function**         | Maps linear combinations to a probability between 0 and 1        |
| \\( \beta_0 \\)                            | ***Intercept***               | Constant term in the model                                       |
| \\( \beta_1 \\)                            | ***Coefficient***             | Weight associated with the predictor variable \( X \)            |

## Components

- **Dependent Variable (Target)**: The binary outcome that is being predicted.
- **Independent Variables (Features)**: Predictor variables used to model the probability of the dependent variable.
- **Logistic Function**: The function used to transform the linear combination of inputs into a probability.

## Training

- **Estimation of Coefficients**: Coefficients \\( \beta_0 \\) and \\( \beta_1 \\) are estimated by maximizing the likelihood function or minimizing the binary cross-entropy loss function. The likelihood function for logistic regression is:

  \\[ L(\beta_0, \beta_1) = \prod_{i=1}^n [P(Y_i = 1 \mid X_i)]^{Y_i} [1 - P(Y_i = 1 \mid X_i)]^{1 - Y_i} \\]

- **Cost Function**: The cost function used is binary cross-entropy:

  \\[ \text{Cost Function} = - \frac{1}{n} \sum_{i=1}^n \left[ Y_i \log(P(Y_i = 1 \mid X_i)) + (1 - Y_i) \log(1 - P(Y_i = 1 \mid X_i)) \right] \\]

- **Optimization**: Coefficients are optimized using techniques such as gradient descent or other numerical optimization methods.

## Importance

- **Binary Classification**: Logistic regression is used to classify data into two distinct classes.
- **Probabilistic Output**: Provides probabilities that allow for the interpretation of predictions and decision-making.
- **Interpretability**: Coefficients represent the effect of each feature on the probability of the positive class, aiding in understanding the model.

## Challenges

- **Linearity Assumption**: Assumes a linear relationship between the predictors and the log-odds of the response.
- **Binary Outcome**: Limited to binary classification; for multiclass problems, extensions like multinomial logistic regression are used.
- **Feature Scaling**: Features may need to be scaled to ensure optimal performance and convergence.

## Applications

- **Medical Diagnosis**: Used to classify patients based on test results and predict the likelihood of diseases.
- **Marketing**: Applied to predict customer responses to promotions or advertisements.
- **Finance**: Helps in credit scoring by classifying applicants as high or low risk.

## Summary

Logistic Regression is a powerful statistical method used for binary classification by modeling the probability of a binary outcome. It applies the logistic function to a linear combination of input features to make predictions. It is valued for its probabilistic output and interpretability but requires attention to its assumptions and limitations.
