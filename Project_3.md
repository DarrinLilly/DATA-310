To complete this project, I started by importing the necessary libraries such as NumPy and TensorFlow. I then import 6,000 of the 10,000 pictures that were provided. The amount of RAM the PyCharm required my computer to have was 30 gigabytes to download all 10,000, which is more than twice the amount I have, so I used 3000 from the Accra1 folder and 3000 from the Accra2 folder to train and test the data. I was also unable to divide the images by 255 because my computer also could not handle doing that process either. Then I created at first a DNN with 3 Dense layers and experimented with the number of neurons I wanted in each layer. I started with having 30 in the first layer, 15 in the second, and 1 in the last one. I experimented with a bunch, but the one that produced the best results was with 5 layers. The top layer had 128, the second had 64, the third had 32, the fourth had 16, and the last had 1. The activation that I went with was ELU, which is an activation that converges the cost function to zero faster. I then compiled the model using stochastic gradient descent as my optimizer function. I tried every optimizer function, and they all produced the same results, but SGD worked the fastest. The loss function I used was mean squared logarithmic error since there were a bunch of different values varying in size; I used this loss function to keep them on the same scale. The metric I used was accuracy.

I tested it using 5 epochs, but after the 2nd epoch, the accuracy was the same. I created a CNN using 3 Conv2d layers with 32 convolutions each, and 3 max-pooling layers. I ran the CNN once, and I took 7 minutes per epoch and got the same results, so I stopped using it.

Attached below are my results.

![Figure_1.png](https://i.loli.net/2020/07/27/mhReQtLixNIJTzM.png)

![Figure_2.png](https://i.loli.net/2020/07/27/IRqGXbau8jsM73B.png)



My model did a very terrible job of predicting the population. I used pictures 4, 267, 476

The actual population was 7.95 my model predicted 0.12

![4.png](https://i.loli.net/2020/08/02/ewJQ7C8aE2hGnz3.png)

The actual population was 0 my model predicted 0.12

![267.png](https://i.loli.net/2020/08/02/AUuitBrl2jWwZ1T.png)

The actual population was 39.95 my model predicted 0.06

![476.png](https://i.loli.net/2020/08/02/2k6X9FW1ivYZDyr.png)