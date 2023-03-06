# Problem Statement

The aim of this task is to develop a feedforward neural network model along with backpropagation algorithm and apply gradient descent (and its variants) for a classification problem. Additionally, we will utilize wandb.ai to keep a record of our experiments and their results.

You can access the task instructions [here](https://wandb.ai/cs6910_2023/A1/reports/CS6910-Assignment-1--VmlldzozNTI2MDc5).


# Installation

Install wandb: 
Install Numpy: 
Install Keras:

# Question 1
Approch:
1. Read input data and create an empty dictionary to store class-wise data.
2. Iterate through the input data and populate the dictionary with images belonging to each class.
3. Initialize an empty list to store the selected images.
4. For each class in the dictionary, select the first image and add it to the list of selected images.
5. Visualize the selected images using library Matplotlib.
6. Integrate Wandb by initializing a new run, logging the selected images.

The code for question 1 is available at the following [link](https://github.com/swapnilmn/Assignment_1-CS6910/blob/master/Assignment_1_Q1.ipynb). Additionally, a WandB visualization for question 1 is accessible at the following [link](https://wandb.ai/ed22s009/Question_1_?workspace=user-ed22s009).

# Question 2
Approch:
1. The code contains a class named "OneHotEncoder_from_scratch" for one-hot encoding of categorical variables.
2. The code defines a class FFNetwork that implements a feedforward neural network for classification tasks.
3. The network is initialized with hyperparameters such as the number of epochs, the number of hidden layers, the size of each hidden layer, the learning rate, and the activation function.
4. The weights and biases of the network are initialized using either random or Xavier initialization.
5. The network has methods for computing the forward activation, gradient of the activation, and softmax function.
6. The forward_pass method computes the output of the network given an input X and the current weights and biases.

The code for question 2 is available at the following [link](https://github.com/swapnilmn/Assignment_1-CS6910/blob/master/Question_2ipynb.ipynb).

# Question 3
Approch:
1. Addition to last question backpropogation added, method performs backpropagation to calculate gradients for each layer of the neural network.
2. The method first performs a forward pass using the input data and current weights. It then computes the derivative of the loss with respect to the final activation layer. Using this derivative, the method iteratively computes the derivatives for each previous layer, propagating backwards through the network.
3. Finally, it returns the derivative of the loss with respect to the input layer activations.
4. The fit method takes input parameters such as X and Y training data, X_val and Y_val validation data, and several hyperparameters such as the optimization algorithm, learning rate, etc.
5. The method trains the neural network for the given number of epochs using a loop and prints the train loss, train accuracy, validation loss, and validation accuracy every five epochs.
6. The method implements four optimization algorithms (SGD, Momentum, RMSProp, Adam) and updates the weights and biases of the neural network in each epoch accordingly.
5. It prints the training and validation loss and accuracy at each epoch.

The code for question 3 is available at the following [link](https://github.com/swapnilmn/Assignment_1-CS6910/blob/master/Question_3.ipynb).

# Question 4
Approch:
1. Initializes Weights and Biases (WandB) to track and visualize training progress.Defines a configuration dictionary containing hyperparameters such as learning rate, number of epochs, optimizer, etc.
2. Defines a train function that initializes WandB with the given configuration, sets up the neural network model, trains the model, and generates a confusion matrix plot.
3. The neural network model is defined using a FFNetwork class, which takes in the given configuration and trains the model using various optimization algorithms such as SGD, Momentum, Adam, etc.
4. The sweep configuration includes the method, name, metric, and parameters for the sweep. The metric used to evaluate the sweep results is val_accuracy, and the goal is to maximize this metric.
5. The parameters in the sweep include epochs, hidden_layer_count, size_hidden_layers, learning_rate, optimizer, batch_size, activation, weight_initializations, and weight_decay. The sweep is created using the sweep_config and run using the wandb.agent() function with the train() function.

The code for question 4 is available at the following [link](https://github.com/swapnilmn/Assignment_1-CS6910/blob/master/Assignment_1_Question4.ipynb). Additionally, a WandB visualization for question 4 is accessible at the following [link](https://wandb.ai/ed22s009/Question_4_Best_Model/reports/Question-4--VmlldzozNzA5ODcx).

# Question 5
The wandb visualisation for question 5 can be found at this [link](https://wandb.ai/ed22s009/Question_4_Best_Model/reports/val_accuracy-v-created-23-03-06-11-49-47---VmlldzozNzA5OTIz?accessToken=cd28z4peh0id23piekqrts0en0v1vzjffn5yie32jpk012ja203h88xh0h0quchc).

# Question 6
The wandb visualisation for question 5 can be found at this [link](https://wandb.ai/ed22s009/Question_4_Best_Model/reports/-23-03-06-11-50-55---VmlldzozNzA5OTMw?accessToken=kgnj99hmixu885d5sy0zgfj8fxqon8ix82e4xwdo04l5s3oxqhprfa0lju24d4ks).


