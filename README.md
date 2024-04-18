# Analysis of Spotify Rhythms

## Overview
This repository contains the Jupyter notebook (predict.ipynb) that demonstrates two objectives:
- Objective 1:
    - Our study strategically analyzes Spotify data to identify the key factors that drive songs to popularity. By quantitatively evaluating popularity and categorizing tracks as either 'popular' or 'not' using a median score, we place particular emphasis on numeric variables that have shown significance in previous studies.
- Objective 2:
    - Our second goal is to redefine genre classification by capturing the actual sound and emotional texture of music, transcending traditional labels, and aligning more closely with the essence of each track by using PC Biplot with K means clustering 

## Dataset
The dataset ”Spotify Tracks” available on Hugging Faces offers a rich repository of audio
features and metadata for a diverse selection of songs on Spotify, covering a wide spectrum of 125 different
genres. With a substantial size of 114,000 rows and 21 columns, this dataset encompasses a plethora of
information about music, including key attributes that define each track.[Spotify Tracks Dataset](https://huggingface.co/datasets/maharshipandya/spotify-tracks-dataset)


## File Structure
- code:
  - predict.ipynb: Jupyter notebook containing all the analysis code, including data preprocessing, model training, evaluation, and prediction.
- code:
  - Spotify Tracking dataset.

## Models
- Regression and  Classification Analysis:
   

### Linear Regression
Linear Regression is used to predict a continuous outcome variable (Y) based on one or more predictor (independent) variables (X). It assumes a linear relationship between X and Y.

### Random Forest
Random Forest is an ensemble learning method for classification and regression that operates by constructing a multitude of decision trees at training time and outputting the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.

### Neural Network
Neural Networks are computing systems vaguely inspired by the biological neural networks that constitute animal brains. They "learn" to perform tasks by considering examples, generally without task-specific programming.

### Logistic Regression
Logistic Regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable, although many more complex extensions exist.

### Bagging and Boosting
Bagging and Boosting are both ensemble techniques to create a strong learning algorithm by combining the predictions from several weak learners. Bagging helps to reduce variance, and Boosting helps to reduce bias in the model.

### Support Vector Machine (SVM)
Support Vector Machine (SVM) is a supervised machine learning algorithm which can be used for classification or regression problems. It uses a technique called the kernel trick to transform the data and then based on these transformations it finds an optimal boundary between the possible outputs.

## Results
Both models were evaluated with the following results:
- Among the regression models evaluated, Random Forest performed best with an MSE of 240.527 and R2 of 0.514, indicating it explained around 51.4% of the variance. Gradient Boosting and SVM had higher MSE (449.519, 459.003) and lower R2 (0.094, 0.075), while Neural Network showed improvement with an MSE of 415.657 and R2 of 0.1, suggesting a moderate understanding of the data’s variance compared to Random Forest
-Among the classification models, the AUC values indicate Neural Network (0.74) outperforms Random Forest (0.71) and Logistic Regression (0.61) in classifying positive and negative classes, with Neural Network showing higher accuracy and precision but slightly lower recall compared to Random Forest.
## Classification of Music genre resulted in building three clusters,
- Energetic Beats (Orange): Songs with high danceability, key, speechiness, and valence, indicating upbeat tracks with clear vocals and positive energy. Medium energy, loudness, mode, and tempo suggest a balanced intensity suitable for various settings.
- Acoustic Mellow (Blue): Characterized by high acousticness and instrumentalness, representing softer, slower tracks with acoustic instruments. Low danceability, energy, key, loudness, and tempo indicate a relaxed listening experience, likely in minor keys for a soothing ambiance.
- Dynamic Rhythms (Green): Featuring medium danceability and energy, these songs offer a blend of dance-friendly beats and engaging listening experiences. High key and tempo suggest lively tracks with faster beats, while low mode and acousticness hint at a focus on electronic sounds over natural instrument



