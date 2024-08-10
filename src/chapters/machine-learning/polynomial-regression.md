# Polynomial Regression

Polynomial regression is a form of regression analysis that models the relationship between the independent and dependent variables as an \( n \)-th degree polynomial. It extends linear regression by fitting a non-linear relationship to the data, allowing for more flexibility in capturing complex patterns.

## Polynomial Regression Formula

The polynomial regression model is an extension of linear regression where the predictors are raised to a power. The formula for a polynomial regression model of degree \( n \) is:

\\[ Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \cdots + \beta_n X^n + \epsilon \\]

where:

- **\\( Y \\)**: Response variable.
- **\\( X \\)**: Predictor variable.
- **\\( \beta_0, \beta_1, \ldots, \beta_n \\)**: Coefficients to be estimated.
- **\\( n \\)**: Degree of the polynomial.
- **\\( \epsilon \\)**: Error term.

### Table of Terms

| Formula                                    | Meaning                | Interpretation                                                     |
|--------------------------------------------|------------------------|---------------------------------------------------------------------|
| \\( Y = \beta_0 + \beta_1 X + \beta_2 X^2 + \cdots + \beta_n X^n + \epsilon \\) | **Polynomial Model**    | Models a non-linear relationship between \( X \) and \( Y \)       |
| \\( \beta_i \\)                            | ***Coefficients***      | Weights for each polynomial term; represents the contribution of each term to the model |
| \\( n \\)                                  | ***Degree of Polynomial*** | Degree of the polynomial; controls the complexity of the model     |

## Components

- **Dependent Variable (Target)**: The variable being predicted.
- **Independent Variable (Feature)**: The predictor variable that is transformed into polynomial terms.
- **Polynomial Terms**: Include higher-order terms of the predictor variable to capture non-linear relationships.

## Training

- **Estimation of Coefficients**: Coefficients \\( \beta_0, \beta_1, \ldots, \beta_n \\) are estimated by minimizing the residual sum of squares. This is done using methods such as Ordinary Least Squares (OLS).

- **Cost Function**: The cost function for polynomial regression is similar to that of linear regression but applied to the polynomial terms:

  \\[ \text{Cost Function} = \|Y - (\beta_0 + \beta_1 X + \beta_2 X^2 + \cdots + \beta_n X^n)\|^2 \\]

- **Optimization**: Finding the optimal coefficients involves solving the optimization problem to minimize the cost function.

## Importance

- **Flexibility**: Polynomial regression can model complex, non-linear relationships that linear regression cannot capture.
- **Curve Fitting**: Allows for fitting curves to data, which can better represent the underlying trends in cases where the relationship between variables is not linear.
- **Predictive Power**: Enhances predictive capabilities for non-linear trends, which can be useful in various fields.

## Challenges

- **Overfitting**: Higher-degree polynomials can lead to overfitting, where the model fits the training data too closely and performs poorly on new data.
- **Model Complexity**: Increasing the degree of the polynomial adds complexity to the model, making it harder to interpret and manage.
- **Feature Scaling**: Higher-order terms may require feature scaling to ensure numerical stability and effective optimization.

## Applications

- **Economics**: Models economic relationships that exhibit non-linear trends, such as income and expenditure patterns.
- **Engineering**: Used in curve fitting for experimental data where the relationship between variables is complex.
- **Biology**: Helps in modeling biological phenomena that follow non-linear growth patterns.

## Summary

Polynomial Regression extends linear regression by incorporating polynomial terms to model non-linear relationships between variables. It provides flexibility in capturing complex patterns but requires careful management of polynomial degree to avoid overfitting and maintain model interpretability. It is useful in fields where non-linear trends are evident and can enhance predictive performance by fitting curves to data.
