# Project summary

The purpose of the project is to detect wheat from a dataset in kaggle.

First, we cleaned the data from bad labels and we used augmentation and CUTMIX to add some noise and unusual data.
In addition, we saw that there is imbalance between the sources of the data so in order to deal with that,
we used stratified 5 Fold and kept in each of the folds with the original ratio between the sources.

We used Faster-r-cnn for detection with ResNet backbones with Feature Pyramid Networks.
The 'train' file purpose is an example of a model which we trained to use in the ensamble.
Our best score on a submitted model (with various types of Hyper-parameters) was 0.62,
which wasnt enough for what we wanted to achieve.

Our idea was to use these trained models to make an ensemble of our models.
The 'inference' file demonstrate how we made the ensemble with the methods that we used including TTA and WBF.
The ensemble improved our score to 0.72 which placed us in the top **20% of the competition.

