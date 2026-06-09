# Hyperparameter Tuning with Keras Tuner

This notebook is about finding the best settings for a neural network automatically, instead of guessing manually.


## What is Hyperparameter Tuning?
 When we build a neural network, we have to make choices like:
  -How many neurons should a layer have?
  -How many layers do we need?
  -Which optimizer should we use?
These choices are called hyperparameters. Instead of trying each one manually, we use Keras Tuner to do it automatically.


## Dataset
Pima Indians Diabetes Dataset - The dataset contains medical diagnostic measurements used to predict whether a patient has diabetes.
Features:
   - Pregnancies
   - Glucose
   - Blood Pressure
   - Skin Thickness
   - Insulin
   - BMI
   - Diabetes Pedigree Function
   - Age

Target Variable:
Diabetes Outcome (0 = Non-Diabetic, 1 = Diabetic)


## What I Did
 -1.Loaded and cleaned the data
 -2.Built a basic neural network first (without tuning)
 -3.Used Keras Tuner to automatically find the best:
   -Optimizer (adam, sgd, rmsprop, adadelta)
   -Number of neurons (searched between 8 and 124)
   -Number of layers (searched between 1 and 10)
 -4.Trained the best model for 100 epochs


## What I Learned
 -Manually picking hyperparameters wastes a lot of time
 -Keras Tuner tries different combinations and picks the best one
 -Small changes in architecture can affect accuracy a lot


##Tools Used
     -Python
     -Pandas, NumPy
     -Scikit-learn
     -TensorFlow / Keras
     -Keras Tuner

## Colab link 
https://colab.research.google.com/drive/1MKH180Kz0JP_VxtCNaNtRL2QERDdSac_?usp=sharing

Date 9/06/2026

Author
Sakshitha | B.Tech CSE | SR University
