# Simple Chatbot with Torch


This app is a chatbot that uses a deep learning model to respond to user inputs. The program is trained using the data in the ``intents.json'' file and gives appropriate answers to the user. In general, this program consists of several key sections:

1. **Data preprocessing**:
    - ``intents.json'' file contains several tags and text patterns (patterns) associated with each tag.
    - The data is parsed into text tokens (words) and converted to word roots using a stemmer.
    - The input data is displayed as a bag of words.

2. **Modeling**:
    - A deep learning model is defined using PyTorch, which includes an LSTM layer and a fully connected layer.
    - LSTM model is used to learn input sequences and better model relationships between words.
    - The output of the model is a probability distribution for each tag.

3. **model training**:
    - The model is trained using training data and optimization with Adam's method.
    - CrossEntropy cost function is used to evaluate the performance of the model.

4. **Prediction and response**:
    - User input becomes a bag of words.
    - The model predicts the most likely output as a label.
    - If the probability of prediction is higher than a certain limit, one of the responses related to that tag is selected from the ``intents.json'' file and displayed to the user


Data:  https://www.kaggle.com/datasets/sheetaljade2019/intentsjson
