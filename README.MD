# **OKCupid Gender Prediction**

## **Project Overview**
This project aims to predict the gender of users from the OKCupid dataset using machine learning models. The dataset includes demographic, lifestyle, and preference-related features. The analysis explores various classification models to determine the best-performing approach. You can find the dataset used compressed in the 'profiles.zip' file.

## **Dataset**
The dataset was sourced from the web and contains the following features:

- **age:** continuous variable of age of user
- **body_type:** categorical variable of body type of user
- **diet:** categorical variable of dietary information
- **drinks:**  categorical variable of alcohol consumption
- **drugs:** categorical variable of drug usage
- **education:** categorical variable of educational attainment
- **ethnicity:** categorical variable of ethnic backgrounds
- **height:** continuous variable of height of user
- **income:** continuous variable of income of user
- **job:** categorical variable of employment description
- **offspring:** categorical variable of children status
- **orientation:** categorical variable of sexual orientation
- **pets:** categorical variable of pet preferences
- **religion:** categorical variable of religious background
- **sex:** categorical variable of gender
- **sign:** categorical variable of astrological symbol
- **smokes:** categorical variable of smoking consumption
- **speaks:** categorical variable of language spoken
- **status:** categorical variable of relationship status
- **last_online:** date variable of last login
- **location:** categorical variable of user locations
- **essay0:** My self summary
- **essay1:**  What I’m doing with my life
- **essay2:** I’m really good at
- **essay3:** The first thing people usually notice about me
- **essay4:** Favorite books, movies, show, music, and food
- **essay5:** The six things I could never do without
- **essay6:** I spend a lot of time thinking about
- **essay7:** On a typical Friday night I am
- **essay8:** The most private thing I am willing to admit
- **essay9:** You should message me if…

## **Preprocessing Steps**
1. **Data Cleaning**: Grouped similar categorical values, converted binary variables, and handled missing values.
2. **Encoding**: One-hot encoded categorical features.
3. **Feature Scaling**: Standardized numerical features.
4. **Splitting Data**: Separated the dataset into training and testing sets.
5. **Hyperparameter Tuning**: Used **GridSearchCV**, **RandomizedSearchCV**, and **BayesSearchCV** to optimize model parameters.

## **Models Used**
We trained four different classification models:

| Model                | Validation Score | Test Score  | Training Time |
|----------------------|-----------------|-------------|---------------|
| Logistic Regression | 0.8653          | 0.8778      | 21s           |
| Decision Tree       | 0.8499          | 0.8567      | 22.3s         |
| Random Forest      | 0.8590          | 0.8691      | 1m 47.3s      |
| SVM                 | 0.8662          | 0.8809      | 2m 52.6s      |

## **Results & Key Findings**
- **Best Model**: Support Vector Machine (**SVM**) achieved the highest test accuracy (**0.8809**) but was computationally expensive.
- **Efficient Alternative**: Logistic Regression performed almost as well (**0.8778**) while being much faster (**21s**).
- **Decision Tree Weakness**: It had the lowest performance and likely overfitted.
- **Random Forest Tradeoff**: Provided a good balance between accuracy and computational time.

## **Next Steps**
1. **Feature Engineering**: Introduce new relevant features, such as profile text analysis (NLP techniques).
2. **Model Optimization**: Apply ensemble learning techniques (e.g., **Stacking, Boosting**).
3. **Computational Efficiency**: Optimize SVM using kernel approximation or explore GPU-accelerated alternatives.
4. **Bias & Fairness Analysis**: Investigate potential biases in predictions to ensure model fairness.
5. **Deploy Model**: Convert the best-performing model into an API for real-world applications.

## **Acknowledgments**
This project was inspired by the OKCupid dataset and serves as a machine learning classification exercise to explore feature preprocessing, model training, and hyperparameter tuning. The dataset was provided by Codecademy.
