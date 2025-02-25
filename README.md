# Building-Feed-Forward-Neural-Networks-FFNNs-from-Scratch-and-FFNNs-for-Sentiment-Classification



1.
Data Processing
Our data set consists of airline reviews. The zip directory for the data contains training and test datasets, where each file contains one airline review tweet. Each of the training data and test data contains 4182 reviews.
a.
Create your Vocabulary: Read the complete training data word by word and create the vocabulary V for the corpus. You must not include the test set in this process. Remove any markup tags, e.g., HTML tags, from the data. Lower case capitalized words (i.e., starts with a capital letter) but not all capital words (e.g., USA). Remove all stopwords. You can use appropriate tools in nltk to stem. Stem at white space and also at each punctuation. In other words, “child’s” consists of two tokens “child and ‘s”, “home.” consists of two tokens “home” and “.”. Consider emoticons in this process. You can use an emoticon tokenizer, if you so choose. If yes, specify which one.
b.
Extract Features: Convert documents to vectors using tf-idf representation. Do not use the existing tf-idf calculation library.
2.
Building FFNNs from Scratch or NN modules and FFNNs for sentiment classification
a.
You will build two FFNN systems using the Sigmod and/or ReLu activation functions:
•
FFNN1: build this system from scratch using only numpy. Do not use any existing libraries, such as scikit-learn or tensorflow/Kereas.
•
FFNN2: build this system using PyTorch.nn or TensorFlow modules. Refer to the provided code examples for guidance.
For each system, set 2 layers with hidden vector size 20. Use sigmoid as the activation function.
b.
Training: Initialize the weights with random numbers. Use Mean Squared Error (MSE) as your loss function You can start training with a learning rate of 0.0001. If you would like to tune any parameters, you must do so using cross-validation on the training data only. Once you have finalized your system, you are ready to evaluate the test data.
Note that if you want to experiment with different stemmers or other aspects of the input features, you must do so on the training set, either through cross-validation or by setting a development set from the get-go. You must not do such preliminary evaluations on test data. Once you have finalized your system, you are ready to evaluate the test data. You can ignore any words that appear in the test set but not the training set.
c.
Evaluation: Compute the most likely class for each review in the test set using each of the combinations of stemming + tf-idf, no-stemming + tf-idf. Compute and report accuracy with confusion matrix on a .txt or .log file.
d.
Comparison: compare the performance of the two systems. Provide explanations at the end of the code file.
