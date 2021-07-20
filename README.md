# Recurrent Neural Networks

![Recurrent Neural Networks: RNN, LSTM, GRU, BiLSTM](rnn.jpg)

Recurrent Neural Networks (RNNs) are a popular model for many NLP tasks as they perform best with sequential data. For this short analysis, we will use a pre-canned IMDB dataset and test the capabilities of a standard RNN, a Gated Recurrent Unit (GRU), a standard Long Short-Term Memory (LSTM), and a bidirectional LSTM. We will then look into the advantages and disadvantages of the architectures. 

## What's an RNN?
RNNs are recurrent, meaning they perform the same task for every element sequence, with the output being dependent on the previous computations. This works similarly to having a memory that logs information. In theory, this architecture can handle arbitrarily long sequences; in practice, the standard RNN suffers from vanishing and exploding gradients. 

The problem with the vanishing gradient is that the RNN becomes incapable of capturing long-term dependencies. The exploding gradient can quickly cause even more problems; potentially, a bad parameter configuration or stochastic gradient descent (SGD) update can become too big, leading to instability in model training. Vanishing gradient problem does not always occur but could contribute to the lower validation accuracy, compared to the others that are preventative of this issue (but it still can occur).

There are ways to fix the vanishing gradient problem; we use ReLU activation functions or change the RNN architecture. For this analysis, we will be changing the architecture and trying to understand why there are differences. 

Let's break down these architectures:

## Long Short-term Memory (LSTM): 
LSTM is a Gated Recurrent Network (GRN) that alleviates some difficulties in training the RNN and deals with the vanishing gradient problem. 

## Gated Recurrent Units (GRU): 
GRU has some advantages over LSTM. GRU has fewer parameters by being a simpler alternative, making it faster to train and perform comparable performance. 

## Bidirectional Long Short-term Memory (BiLSTM):
Two hidden states created from both LSTMs are concatenated. This gives the NN more representational power by looking into the past and future contexts by looking at both left and the right context for the current prediction. 
