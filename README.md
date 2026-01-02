# Laptop price prediction model
## User instructions
To install the necessary libraries type
`pip install -r requirements.txt` in the terminal git

## Problem Statement
Build a model to predict a laptop's price based on relevant features with minimal error

## Approach
I trained the model with features such as Processor speed, ram size, storage capacity, screen size and weight. The data was split into training and testing sets and was trained using linear regression. I have also regularized the features so that there is no overfitting problems. I have given the feature imporance in descending order below : 

Feature - importance (Descending order)
| Feature          | Coefficient (Importance) |                        
| ---------------- | ------------------------ | 
| Storage_Capacity | **9348.26**<--- Strongest contributor to laptop price              | 
| RAM_Size         | **552.43**               |
| Processor_Speed  | **144.07**               | 
| Screen_Size      | **33.19**                | 
| Weight           | **-5.80** <--- Negligible impact on price               | 

## Graph of predicted price vs actual price
<Figure size 640x480 with 1 Axes><img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/fce13190-06d3-44e5-ab1a-5c1413b39281" />

## Results
We have two models, one with regularization and one without regularization. I have given results of both the models below : 

`Baseline r2 score :  0.9996472163447738`

`Baseline mse score :  32031.539130628313`

`Regularized model r2 score :  0.9996474160745367`

`Regularized model MSE score :  32013.40435704242`

We notice that there isn't much of a difference between the scores of the regularized model and the non-regularized model. The key idea we get from this particular result is that regularization helps only when there are many irrelevant features or unstable coefficients. But we have already noticed that the strongest feature "Storage Capacity" far outweighs the other features in terms of importance. Hence, there isn't much of a difference between the baseline and regularized model.





