# Regression

### Linear Regression

Linear regression is a statistical method that explores the relationship between two variables. It provides a model that can be used to predict the value of a response variable based on the value of a predictor variable.

A **regression equation** is used in statistics to __determine the nature of the relationship between variables__ and to predict the values of one variable based on the values of another.

A ***regression line*** is a line that best fits the data points in a scatterplot, representing the best estimate of the relationship between the variables.

#### Linear Regression Formula

The formula for a simple linear regression model is:

\[ Y = mX + b \]

where:

- **\( Y \)**: The response variable (dependent variable) that you are trying to predict.
- **\( X \)**: The predictor variable (independent variable) used to make predictions.
- **\( m \)**: The slope coefficient, which represents the change in \( Y \) for a one-unit increase in \( X \).
- **\( b \)**: The intercept parameter, which represents the value of \( Y \) when \( X \) equals 0.

#### Table of Terms

| Formula   | Meaning                | Interpretation                                                      |
|-----------|------------------------|----------------------------------------------------------------------|
| `Y = mX + b` | **Formula**            | The equation of the regression line                                 |
| `m`       | ***Slope Coefficient*** | Indicates the estimated change in \( Y \) for a one-unit increase in \( X \) |
| `b`       | ***Intercept Parameter*** | Represents the estimated value of \( Y \) when \( X \) equals 0      |

#### Additional Details

- **Fit of the Line**: The goal of linear regression is to find the line that best fits the data points. This is usually done by minimizing the sum of the squared differences between the observed values and the values predicted by the model.
- **Interpretation**: The slope coefficient \( m \) tells us how much \( Y \) is expected to increase (or decrease) for each unit increase in \( X \). The intercept \( b \) provides a baseline value of \( Y \) when \( X \) is zero, which helps in understanding the starting point of the relationship.
- **Prediction**: Once the regression line is determined, it can be used to predict \( Y \) for any given value of \( X \). This is useful in various fields like finance, economics, and the natural sciences.
