# Seattle-House-Price-Prediction-Machine-Learning-
This project builds and evaluates machine learning models to predict house prices in the Seattle area using structural and location-based features. The goal is to understand which features drive housing prices and to build a model that generalizes well to unseen data.

Abstract

This project explores the use of machine learning techniques to predict residential house prices in the Seattle area using structured housing data. Multiple regression models were developed, evaluated, and compared to identify the most effective approach for minimizing prediction error. Emphasis was placed on proper data preprocessing, feature selection, model validation, and error analysis to ensure robust and generalizable results.

Introduction

Accurately predicting house prices is a classic regression problem in data science with real-world applications in real estate, finance, and urban planning. Housing prices are influenced by a combination of structural characteristics, location-based factors, and nonlinear interactions between features. The objective of this project was to build an end-to-end machine learning pipeline capable of predicting house prices while identifying the most influential features driving those predictions.

Data and Feature Selection

The dataset consisted of approximately 21,000 residential properties from the Seattle area, with a mean sale price of $540,088. The target variable was the sale price, while input features included structural attributes such as living area square footage, construction grade, number of bathrooms, and number of floors, as well as location-based variables such as latitude and waterfront presence.

Initial exploratory data analysis included correlation analysis to understand linear relationships between features and the target variable. Features with stronger predictive potential, such as sqft_living, grade, and sqft_above, were selected, while non-informative identifiers were excluded to prevent data leakage.

Modeling Approach

Several supervised learning models were implemented and evaluated. A Decision Tree Regressor was first used as a baseline due to its interpretability and ability to model nonlinear relationships. However, initial results revealed overfitting, which was mitigated through hyperparameter tuning, specifically by constraining the number of leaf nodes.

To improve performance, a Random Forest Regressor was implemented. This ensemble method combines multiple decision trees trained on bootstrapped samples and averages their predictions, significantly reducing variance and improving generalization. Hyperparameters such as the number of trees and tree depth were adjusted to optimize performance.

Model Evaluation and Validation

Model performance was evaluated using Mean Absolute Error (MAE), an intuitive metric that measures average prediction error in dollar terms. A train-validation split was used initially, followed by cross-validation to assess model stability and robustness across multiple folds.

The Random Forest model achieved a validation MAE of approximately $91,550, representing a substantial improvement over the baseline decision tree model. Relative to the mean house price, this corresponds to an error rate of approximately 17%, which is considered strong performance for tabular housing data without external market features.

Error Analysis and Interpretability

Feature importance analysis was conducted to interpret model behavior. Results showed that square footage and construction grade were the most influential predictors, while bedroom count had a smaller marginal impact once size was accounted for. Location features contributed nonlinearly to predictions, highlighting the importance of spatial information.

Error analysis revealed that the model tended to underpredict higher-priced luxury homes, a common limitation in housing models due to skewed price distributions. This insight motivated consideration of log-transforming the target variable and additional feature engineering for future improvements.

Conclusion

This project demonstrates a complete data science workflow, including exploratory data analysis, feature selection, supervised learning, hyperparameter tuning, cross-validation, and model interpretation. By leveraging ensemble methods such as Random Forests, the model significantly improved predictive accuracy over simpler approaches. The techniques applied in this project reflect real-world data science practices and provide a strong foundation for further work in predictive modeling and applied machine learning.
