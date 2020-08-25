# Learn the alphabet using Recurrent Neural Network

alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
Credit: Deep Learning with Python by Jason Brownlee  

## 1. alphabet_LSTM_1to1  for  Learning  One-Char  to  One-Char  Mapping, 1 to 1
<img src = "https://github.com/sindhri/learn_alphabet/blob/master/doc/img1.png" width = "250">
500 epochs, took a while to train
Model Accuracy: 84.00%

## 2. alphabet_LSTM_3to1 for 3 to One-Char Mapping, 3 to 1
<img src = "https://github.com/sindhri/learn_alphabet/blob/master/doc/img2.png" width = "250">
Fast 
Model Accuracy: 82.61%

## 3. alphabet_LSTM_3stepsto1 for a time steps to One-Char Mapping, 3 to 1
Same as the above model, but the input data was shaped differently, so that the previous information is modeled as time steps, instead of window features
Model Accuracy: 95.65%

## 4. alphabet_LSTM_batchto1 with a larger batch
Same as 1to1, but a larger batch that is the same size as the input.
Fast!
100.00%

## 5. alphabet_LSTM_statebatchto1 with state! (How LSTM is meant to be used)
Very fast!
Model Accuracy: 100.00%

## 6. alphabet_LSTM_varto1 stateless variable length to One-Char Mapping
<img src = "https://github.com/sindhri/learn_alphabet/blob/master/doc/img7.png" width = "250">
Very Very slow.  
Model Accuracy: 98.40%. Maybe it learned something!


# Conclusion: LSTM with state has the best performance and speed, but it may not have learned the generic information. Stateless LSTM performs the best without knowing the whole sequence. 