# AI-Powered Dirt Bike Recommender: Final Report

## **Define the Problem Statement**

This project's goal is to develop an AI-driven machine learning solution that recommends suitable dirt bikes for beginner riders. New riders often face challenges in selecting an appropriate first bike from a wide range of options, and an incorrect choice can negatively impact their safety, confidence, and overall enjoyment of the sport. The primary benefit of this solution is to provide personalized and safe recommendations that enhance a beginner's initial riding experience.

***

## **Model Outcomes or Predictions**

The model will utilize **supervised learning** algorithms. The problem is framed as a **classification task**, where the model will learn from various rider and bike attributes to predict the most suitable bike for a user.

The expected output of the model will be a specific bike recommendation or a category of bike (e.g., "small trail bike") that is best suited to the beginner rider's profile.

***

## **Data Acquisition**

To ensure the best results, data will be acquired from multiple sources. The key datasets required for this model are:

* **Rider Profile Data**: This includes personal attributes such as age, height, weight, and previous riding experience (e.g., none, bicycle, ATV).
* **Dirt Bike Specifications Data**: This dataset will contain key details about different bike models, including engine size (cc), seat height, bike weight, and the target rider skill level.
* **Expert Recommendations and Historical Data**: This data will be sourced from experienced instructors and rider reviews to serve as the "ground truth" for training the model.

A preliminary analysis suggests that rider attributes like height and experience level will have the most significant impact on the final recommendation, as illustrated in the feature importance chart below.



***

## **Data Preprocessing/Preparation**

To prepare the data for modeling, the following preprocessing steps will be performed:

* **Data Cleaning**: The acquired datasets will be checked for missing values and inconsistencies. Missing numerical data will be handled using imputation (e.g., filling with the median value), while missing categorical data will be imputed with the mode.
* **Feature Encoding**: Categorical features from the Rider Profile Data, such as 'experience' and 'intended riding terrain', will be converted into a numerical format using one-hot encoding so they can be effectively used by the machine learning algorithm.
* **Train-Test Split**: The final, cleaned dataset will be split into a training set (80% of the data) and a test set (20% of the data). This allows the model to be trained on a majority of the data and then evaluated on unseen data to test its real-world performance.

***

## **Modeling**

Multiple machine learning algorithms were considered for this problem. The selected algorithm for the initial model is a **Decision Tree**.

A Decision Tree model was chosen primarily because it offers transparent and easily explainable recommendations. Given that the recommendations are for beginner riders, the ability to understand the logic behind a suggestion (e.g., "this bike is recommended because of your height and lack of experience") is crucial for building user trust and ensuring safety.

***

## **Model Evaluation**

The models considered for this problem included classification, regression, and recommender systems. Since we have framed this as a classification task, the model's performance will be evaluated using the following metrics:

* **Accuracy**: The percentage of correct recommendations made by the model.
* **Precision**: Measures the proportion of recommended bikes that are actually suitable. High precision is critical to avoid making unsafe recommendations.
* **Recall**: Measures the proportion of all suitable bikes that the model successfully identifies.
* **F1-Score**: The harmonic mean of precision and recall, which provides a single, balanced score of a model's performance.

The optimal model will be the one that achieves the highest F1-Score, with a strong emphasis on **Precision**. This ensures that the recommendations provided to beginner riders are not only relevant but, most importantly, safe and appropriate for their skill level.
