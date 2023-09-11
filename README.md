# Neural_net_from_scratch

## IMPORTING LIBRARIES
### TENSORFLOW : 
### NUMPY :
### MATPLOTLIB :
### NN_UTILS :
### % matplotlib inline : 
The %matplotlib inline magic command is used in Jupyter Notebook and JupyterLab environments to display   matplotlib plots directly within the notebook interface.

## INITIALIZING NEURAL NETWORK
* layers => no.of layers(L), no.of features(num_features), no.of classes(num_classes)
  for example : net=NeuralNetwork([10, 30, 100, 10])
  ![Illustation](images/layers_array.jpeg)
* Track of parameters(weignts , biases) and graients(dW , db)
* Setup() => initializing parameters.
  size of parameters W and B:
  ![source:https://www.deeplearning.ai](images/size_of_parameters.jpeg)
* ##### tf.random.normal(shape=(self.layers[i], self.layers[i-1]))
  generates random values following a normal distribution with a shape determined by self.layers[i] and self.layers[i-1]. This is typically used to initialize the weights with random values.
* ##### tf.Variable() 
  wraps this random weight matrix in a TensorFlow variable, making it trainable during the model’s training process. The weights in this matrix will be updated as the model learns from the data.

## FORWARD PROPAGATION
* Z = W.X +b
  Till last layer : activation function used => relu
  IN the last layer : softmax or sigmoid(for binary classification)
  In this code, we have left last layer without applying any activation function which we will do it later.