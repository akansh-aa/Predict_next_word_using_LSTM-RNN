“LSTM (Long Short-Term Memory) is utilized for modeling long-term dependencies in sequential data or sequence of words , allowing it to capture and remember information over extended periods within a sequence.”

Why use LSTM?
Vanishing gradient descend is a problem faced by neural networks when we go for backpropagation as discussed here. It has a huge effect and the weight update process is widely affected and the model became useless. So, we used LSTM which has a hidden state and a memory cell with three gates that are forgotten, read, and input gate.

![image](https://github.com/user-attachments/assets/5f4dd4da-8b79-48cd-b66f-e3814f1ed82c)


The forget gate is mainly used to get good control of what information needs to be removed which isn’t necessary. Input gate makes sure that newer information is added to the cell and output makes sure what parts of the cell are output to the next hidden state. The sigmoid function used in each gate equation makes sure we can bring down the value to either a 0 or 1.

The exact model architecture of an LSTM is shown in this figure. Here, X is the word subscript t indicates that time instant. As we can see, c and h are input coming from an earlier time or the last step. We have the forget gate that controls the weights so that it can exactly know what information needs to be removed before going to the next gate. We use sigmoid here. The input I am added and some new information is written in the cell at that time instant. Finally, the output gate outputs the information that is given to the next LSTM cell.

![image](https://github.com/user-attachments/assets/3eaa40b0-0744-48a6-b89a-41585e822740)


Num of layers:
The number of layers in an LSTM network is a hyperparameter that can be tuned to improve the performance of the network. The number of layers determines the depth of the network, and a deeper network can learn more complex relationships in the data. However, a deeper network also requires more training data and can be more difficult to train.

Num of units:
The number of units in an LSTM layer is another hyperparameter that can be tuned to improve the performance of the network. The number of units determines the width of the network, and a wider network can learn more complex relationships in the data. However, a wider network also requires more training data and can be more difficult to train.

Prediction of next word
Predicting the next word is a neural application that uses Recurrent neural networks. Since basic recurrent neural networks have a lot of flows we go for LSTM. Here we can make sure of having longer memory of what words are important with help of those three gates we saw earlier.

![image](https://github.com/user-attachments/assets/8dfbe2c0-a34e-45a2-a188-c694620efa66)

