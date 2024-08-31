# Detecting spam emails with Long Short-Term Memory (LSTM) networks.
Long Short-Term Memory (LSTM) networks are a special category of Recurrent Neural Networks (RNN) [1]. RNNs deal with sequential data, such as time-series or texts. LSTM tries to alleviate vanishing gradients found in traditional RNN training. They also treat "memory" (especially short-term memory) in a more delicate way. For more details, you can read the original cited paper.

In order to respect the semantic relationships between words the GloVe word embedding model was used [2]. The data I used in this demo come from Kaggle [3]. It can be easily accessed and downloaded.

Since all of the training & testing happens within the Jupyter notebook, the only thing you have to do to run this code is to download the notebook `spam_detection_LSTM_01.ipynb`, the dataset `emails.csv`, and the word embeddings file `glove.6B.100d.txt` (which you can find online and download) in the same directory (or in different directories, as long as you change the path to the *csv file), and create a virtual environment with numpy, pandas, matplotlib, PyTorch (as of July 2024, the latest versions are all fine, previous and future versions should also work). 

This is the first demonstration of my LSTM model. In the notebook, I describe the process step-by-step, and I often mention what went wrong the first times I attempted to train the model and I failed. **In the future, I want to conduct a more thorough and careful evaluation of the model, as well as re-train the model on my collection of spam and non-spam emails I have received.** (right now it seems like most spam emails in the dataset include unknown words, so the model is biased against texts with unknowns words and labels them as spam)

### Libraries
- numpy
- matplotlib
- pandas
- PyTorch

## References and Sources
<a id="1">[1]</a> 
Hochreiter, S., & Schmidhuber, J. (1997). Long short-term memory. Neural computation, 9(8), 1735–1780. https://doi.org/10.1162/neco.1997.9.8.1735

<a id="2">[2]</a>
[GloVe: Global Vectors for Word Representation](https://aclanthology.org/D14-1162) (Pennington et al., EMNLP 2014)

<a id="3">[3]</a>
https://www.kaggle.com/datasets/jackksoncsie/spam-email-dataset
