# Practical-Application-III-Comparing-Classifiers

I was able to successfully create several models that were able to correctly identify customers who would respond positively to the marketing campaign. I applied a grid search technique to try combinations of parameters for the model algorithms, which did create a slight improvement in the models' performance, particularly for how they performed on the test data. In addition, I tried a second grid search technique, the Randomized Search CV method, to see how much it improved the run times and whether it suggested the same parameters.

## Findings

The models' scores are summarized below. All models performed well, but only SVM was better than my baseline logistic regression and is my initial choice of model. Considering the additional training time needed for SVM, however, it would not be as good of a choice for larger datasets. 

![Screenshot 2024-07-06 151426](https://github.com/SenorMega/Practical-Application-III-Comparing-Classifiers/assets/161073693/62741515-7ecd-4366-ad94-0b13d2bc2c57)



Here is a summary of the accuracy scores for each of the three model types that I trained, before and after using grid search to optimize their parameters. Note that the improved parameters from the grid search all produced worse results than the default settings for the training scores, but improved results for their test scores. The effect was especially strong for the decision tree model, improving from last to first place in test accuracy score.

After optimizing the models, it is clear that a Decision Tree model is best for this dataset. It has both the best accuracy and by far the shortest training times. 

![Screenshot 2024-07-06 150438](https://github.com/SenorMega/Practical-Application-III-Comparing-Classifiers/assets/161073693/d1ba69e6-8f47-4262-b8c9-994bc689705a)



Using Randomized Search CV produced the same parameter suggestions while taking significantly less time. It was a helpful exercise to do this, but using the decision tree model renders it mostly moot because of its very quick train time. Regardless, the differences in search times are shown in this graph:

![Screenshot 2024-07-06 150506](https://github.com/SenorMega/Practical-Application-III-Comparing-Classifiers/assets/161073693/69230462-8e24-465c-aa10-9e2d3bfdcdda)


