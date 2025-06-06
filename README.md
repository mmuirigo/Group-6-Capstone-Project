# Recipe Recommender System  <img src="https://raw.githubusercontent.com/mmuirigo/Group-6-Capstone-Project/main/plate.png" alt="Plate" width="100"/> 
## Business Understanding
Preparing meals is often a challenge due to diverse individual preferences, dietary needs, and varying ingredient availability. This project aims to address these issues by developing a Personalized Recipe Recommendation System using Machine Learning and Natural Language Processing (NLP).
## Problem Statement
To develop a Personalized Recipe Recommendation System that leverages Machine Learning and NLP techniques to provide customized recipe suggestions based on user preferences, ratings, and recipe content.
### Objectives
- To develop a content-based model using NLP to recommend recipes based on ingredients and instructions.
- To build a collaborative filtering model using user ratings and interactions.
- To combine both approaches into a hybrid recommendation system.
- To evaluate model performance
### Dataset Source
  The project uses the [Food.com Recipes and Reviews dataset](https://www.kaggle.com/datasets/irkaal/foodcom-recipes-and-reviews) from Kaggle.
   -   Recipes dataset: 522,517 recipes
   -   Reviews dataset: 1.4M user reviews,ratings & comments.
# Data Cleaning 
- Missing data handling
- Data types harmonization including time conversion
- Deduplication
- Feature Engineering
- Slicing the dataset for optimal performance
## Exploratory Data Analysis
- Quick Descriptive analysis of both categorical and numerical variables
- Visualize specific variables of importance to the exercise and evaluate the relationship
  ### Popularity
     ![Recipe Popularity](https://github.com/mmuirigo/Group-6-Capstone-Project/blob/main/Popularity.png)
  ### Number of Recipes per year
    ![Popularity](https://github.com/mmuirigo/Group-6-Capstone-Project/blob/main/RecipePerYear.png)

  ### Nutritional Correlation matrix
    ![Nutritional](https://github.com/mmuirigo/Group-6-Capstone-Project/blob/main/Nutritional.png)
  
   ### Top 10 words from the Ingredient list
    ![Ingredients](https://github.com/mmuirigo/Group-6-Capstone-Project/blob/main/Top10Ingredients.png)

# Modeling
- **Collaborative Filtering** Implement Collaborative Filtering that makes recommendations by learning patterns from user behavior. It recommends items liked by similar users.
- **Implement Content-Based recommendation** system using TF-IDF and Nearest Neighbors. This recommends recipes that are similar in content to what the user likes.
- **Deep Learning Model** The Deep Learning Recommender system uses neural networks to learn complex patterns between users and items. It will learn non-linear relationships between users and items.
- **The hybrid model** combined collaborative filtering with content-based features. It uses User ID, Recipe ID and Prep time (TotalTimeMinutes) as content feature.The model learns both user preferences (who likes what) and recipe attributes (like prep time) to make better predictions.It learns a dense vector (embedding) for: Each user (how they behave) and Each recipe (how it's rated). These embeddings capture hidden patterns in the data.

# Summary
Four recommendation models were implemented and evaluated: collaborative filtering (SVD), content-based filtering, a deep learning model, and a hybrid model. Performance was measured using RMSE, MAE, and Precision@5, along with TensorBoard visualizations for training behavior.
- Collaborative Filtering (SVD) achieved an RMSE of 1.9881 and MAE of 1.6032, indicating moderate prediction error and suggesting room for improvement through tuning or incorporating side features.
- Content-Based Filtering showed good precision with a Precision@5 of 0.6971, meaning it was effective at recommending relevant items within the top 5 results, though limited by a lack of collaborative signals.
- The Deep Learning Model (matrix factorization-based) performed less effectively with an RMSE of 2.1843, likely due to overfitting or insufficient feature diversity.
- The Hybrid Model, combining user-item embeddings with content features (like preparation time), significantly outperformed all others with an RMSE of 0.3757. TensorBoard confirmed better generalization, smooth loss convergence, and a balanced parameter distribution.

## Conclusion:
The **Hybrid Model** proved to be the most robust and accurate, leveraging the strengths of both collaborative and content-based methods for optimal recommendation performance.

  ### Authors 😄
|Neema|Susan|
|George|Valentine|
|Mourine|
