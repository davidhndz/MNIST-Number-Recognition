## Number Recognition (MNIST Data Set)

### My reason for the project

This is a small project I took on to use tensorflow to build a neural network using tensorflow. 
I had initially built this project using numpy and matplotlib without an AI library. The idea of the neural network is simple enough to not need a library.

Basically it takes in the 28 x 28 image and flattens it into an array, it feeds that image data (about 784 pixels into the neural network and through several hidden layers.
The hidden layers use ReLU as an activation function to add complexity, and going through each layer we can image each neuron represents more abstract features of these numbers.
This all leads to the output layer where we use the softmax activation function in order to represent the data as a certainty, the node with the highest number in the activation function is the one the NN thinks the input most likely is.

The model is then trained using the adam optimizer and the loss function of sparse categorical crossentropy. I honestly am not as familiar with this part of the network.
I know that adam optimzer is the most widely use training optimizer, and have looked into the math but couldnt specifically tell you why.
The loss function of cross entropy I cannot speak on as I really have no idea, and is something to look into.

Once the model is trained it is saved in the local folder for later use, even with the quick creation of this model and the small ammount of training sessions it reaches an accuarcy of 97% on training data.
However when trained on new handmade images I find that it struggles, further likely because of overfitting and being used to the style of numbers found in the data set.
In one instance a really round top to the number 9 had the model confused and it instead chose an 8. It is my hypothesis that the model has a bias for features like that and could possibly benefit from dropout.

Overall this was not a difficult small project, in the future I want to become more familiar with tensor flow and implement it on my own using a CNN with image convolution and pooling
I also want to make this more interactable by creating a front end pygame app that will allow you to draw and image and the model to tell you what number it is.
