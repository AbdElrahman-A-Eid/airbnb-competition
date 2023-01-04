# Airbnb: New User Bookings | Kaggle Competition
My Solution to Airbnb: New User Bookings Competition on [Kaggle](https://www.kaggle.com/competitions/airbnb-recruiting-new-user-bookings)

# Introduction
## What is Airbnb?
- [Airbnb](https://www.airbnb.com/) is an **online platform** where people can list
or rent properties for **short-term use**. Be it an entire
home, a spare bedroom or even a sofa, anyone
looking to earn some profit can promote their space
on Airbnb.
- New​ users​ on​ Airbnb​ can​ book​ a place​ to​ stay​ in​ *34,000+ cities*​ across​ *190+​ countries*.
- The platform was launched in **2008**.

## Problem Category
Multiclass Classification

## Problem Statement
Given a list of users along with their demographics, web session records, and some summary statistics, the objective is to **predict the top 5** travel destinations in decreasing order of relevance for each of the new user.

# Dataset
## Stats
- Observations:
    - Training Users: 213,451
    - Test Users: 62,096
    - Session Records: 10,567,737
- Features: 
    - users: 15
    - sessions: 6
## Files Description
- **train_users_2.csv** - the training set of users
- **test_users.csv** - the test set of users
    - **id**: user id
    - **date_account_created**: the date of account creation
    - **timestamp_first_active**: timestamp of the first activity, note that it can be earlier than date_account_created or date_first_booking because a user can search before signing up
    - **date_first_booking**: date of first booking
    - **gender**
    - **age**
    - **signup_method**
    - **signup_flow**: the page a user came to signup up from
    - **language**: international language preference
    - **affiliate_channel**: what kind of paid marketing
    - **affiliate_provider**: where the marketing is e.g. google, craigslist, other
    - **first_affiliate_tracked**: whats the first marketing the user interacted with before the signing up
    - **signup_app**
    - **first_device_type**
    - **first_browser**
    - **country_destination**: this is the target variable you are to predict
- **sessions.csv** - web sessions log for users
    - **user_id**: to be joined with the column 'id' in users table
    - **action**
    - **action_type**
    - **action_detail**
    - **device_type**
    - **secs_elapsed**
- **countries.csv** - summary statistics of destination countries in this dataset and their locations.
- **age_gender_bkts.csv** - summary statistics of users' age group, gender, country of destination.
- **sample_submission.csv** - correct format for submitting your predictions.

# Libraries Used
- SciKit-Learn
- NumPy
- Pandas
- SciPy
- XGBoost
- Visualization:
    - Matplotlib
    - Seaborn

# Model Approach
- [XGBoost](https://xgboost.readthedocs.io/en/stable/) Classifier
- Extended Hyperparameter Tuning
- Cross Validation
- [NDCG](https://en.wikipedia.org/wiki/Discounted_cumulative_gain#Normalized_DCG) Evaluation Metric

# Model Performance
- Training Score: 83.07%
- Test Score: 88.13%

View the notebook on [Kaggle](https://www.kaggle.com/code/yinshe/extreme-hyperparameter-tuning).