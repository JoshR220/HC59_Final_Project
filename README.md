

# HC59_Final_Project
Final Project for HC59


In the course of this github repo I will attempt to extend the applications of the QISKIT tutorial on using quantum circuits along with traditional machine learning methods. In this tutorial a quantam-classical hybrid convolutional neural network is used on the MNIST dataset. The MNIST dataset is a collection of 28x28 greyscale handwritten digits from 0-9. Traditional convolutional neural networks have been well-applied to this dataset with extremely accurate results. An example MNIST digit (expanded for visual purposes) is pictured below.


![MNIST Digit](https://github.com/JoshR220/HC59_Final_Project/blob/main/images/MNIST_figure.png)


The demonstration of the hybrid network is to illustrate that quantum components can be used within the traditional network and still output a working result. Essentially, we want to show that the output of the classical network is not signficantly degraded after being feed into the quantum network. Whether quantum computers can have an advatnage over classical models is yet to be determined, but the first step is to illustrate that quantum is as good or only slightly worse than classical models. A depiction of a hybrid network from the Qiskit texbook is below. 

![layers](https://github.com/JoshR220/HC59_Final_Project/blob/main/images/layers_qiskit.png)

The greatest difference between the classical and quantum machine learning components is the computation of gradients for backpropogation. Quantum circuits use the parameter shift rule in order to calculate gradients. The Qiskit textbook shows the gradient rule as below. 

![gradient](https://github.com/JoshR220/HC59_Final_Project/blob/main/images/quantumgradient.png)

Essentially, all that occurs is that you shift the parameters of the quatum circuit one way and obatin a result, then shift the parameters the opposite way and obtain that result. The gradient is then the difference between those two results! This rule allows us to run loss functions on the quantum component of the network and tune the parameters to reduce loss. 

Given all the above information, the goal of this repsitory is expanding on the tutorial in the Qiskit textbook. Currently, the Qiskit tutorial only creates a hybrid network that learns to distinguish between the digits 0 and 1 and show that the hybrid network can well distinguish between the two digits after training- it is actually able to practically 100% determine the two digits after training. My goal is to expand this circuit to at least 4 digits- 0,1,2,3- and potentially add entanglement to see if that has an effect on the results of the hybrid network compared to a classical CNN. 

I was unable to properly train the hybrid network for more than 2 digits. I had an accuracy hovering in the range of 25% for classification between 0,1,2,3- no better than guessing. My belief is that the gradient backpropagation isn't working properly and thus the network fails to train accordingly. Moving forward my goal would be to better integrate and develop the backpropagation feature in the hybrid network class. 
 
 (Pictures from Qiskit textbook and MNIST dataset)
