# SERModel
This repository contains code and data for a speech emotion recognition system. The system is based on a deep learning model that has been trained on a dataset of audio recordings and their corresponding emotional labels



Building Models
Since the project is a classification problem, Convolution Neural Network seems the obivious choice. We also built Multilayer perceptrons and Long Short Term Memory models but they under-performed with very low accuracies which couldn't pass the test while predicting the right emotions.

Building and tuning a model is a very time consuming process. The idea is to always start small without adding too many layers just for the sake of making it complex. After testing out with layers, the model which gave the max validation accuracy against test data was little more than 70%

Feature Extraction
The next step involves extracting the features from the audio files which will help our model learn between these audio files. For feature extraction we make use of the LibROSA library in python which is one of the libraries used for audio analysis.

Predictions
After tuning the model, tested it out by predicting the emotions for the test data. For a model with the given accuracy these are a sample of the actual vs predicted values.


Testing out with live voices.
In order to test out our model on voices that were completely different than what we have in our training and test data, we recorded our own voices with dfferent emotions and predicted the outcomes. You can see the results below: The audio contained a male voice which said "This coffee sucks" in a angry tone.



As you can see that the model has predicted the male voice and emotion very accurately in the image above.
NOTE: If you are using the model directly and want to decode the output ranging from 0 to 9 then the following list will help you.
0 - female_angry
1 - female_calm
2 - female_fearful
3 - female_happy
4 - female_sad
5 - male_angry
6 - male_calm
7 - male_fearful
8 - male_happy
9 - male_sad

Conclusion
Building the model was a challenging task as it involved lot of trail and error methods, tuning etc. The model is very well trained to distinguish between male and female voices and it distinguishes with 100% accuracy. The model was tuned to detect emotions with more than 70% accuracy. Accuracy can be increased by including more audio files for training.
