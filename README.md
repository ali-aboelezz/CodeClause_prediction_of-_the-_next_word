# Prediction of the  next Word

### Next Word Prediction:
   Next Word Prediction is an application of NLP (Natural LanguageProcessing). It is also known as Language Modeling. Basically it is the process of predicting the next word in a sentence. It has many applications which are used by most of us such as auto-correct which is mostly used in Emails / Messages; it has also it’s usage in MS Word or google search where forecasts the next word based on our search history or the search we did for globe. In this work we have studied NLP, different deep learning techniques such as LSTM.

### We Will Use LSTM:  
The model we’ll build will correspond to the diagram above. The three key components are an embedding layer, the LSTM layers, and the classification layer. We already know the purpose of the LSTM and classification layers. The purpose of the embedding layer is to map each word (given as an index) into a vector of E dimensions that further layers can learn from. Indecies or equivalently one-hot vectors are considered poor representations because they assume words have no relations between each other. This mapping is also learnt during training.


## About Dataset:


- We will use the datasets library from HuggingFace to load and map over the dataset, Torchtext to tokenize the dataset and construct the vocabulary and PyTorch to define, train and evaluate the model.

- To load the dataset, we use the load_dataset() function from datasets. There are two WikiText datasets, an older version: WikiText-103 and a newer version: WikiText-2. For each there is a raw version and a slightly-preprocessed version. We have chosen the raw version of the newer dataset because we will take care of preprocessing by ourselves later.

## Prerequisites:
You’ll need to install the following libraries with pip:

!pip install Torchtext

- to get the dataset:

!pip install datasets





## Libraries Used

- [Numpy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [PyTorch](https://pytorch.org/)


## Conclusion
- Once trained, the model has a sense of the probability of different sequences. Thus, given an initial set of tokens the model can generate subsequent tokens so that the sequence in the end makes sense.

- Given a large corpus of text, we need to tokenize it, encode it and put it in the right shape before we start training.

- We also save the model with the highest validation loss and return the perplexity which an increasing function of the loss that measures how confident the model is.
