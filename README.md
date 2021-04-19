

# HC59_Final_Project
Final Project for HC59


In the course of this github repo I will attempt to extend the applications of the QISKIT tutorial on using quantum circuits along with traditional machine learning methods. In this tutorial a quantam-classical hybrid convolutional neural network is used on the MNIST dataset. The MNIST dataset is a collection of 28x28 greyscale handwritten digits from 0-9. Traditional convolutional neural networks have been well-applied to this dataset with extremely accurate results. An example MNIST digit (expanded for visual purposes) is pictured below.


![MNIST Digit](https://github.com/JoshR220/HC59_Final_Project/blob/main/images/MNIST_figure.png)


The demonstration of the hybrid network is to illustrate that quantum components can be used within the traditional network and still output a working result. Essentially, we want to show that the output of the classical network is not signficantly degraded after being feed into the quantum network. Whether quantum computers can have an advatnage over classical models is yet to be determined, but the first step is to illustrate that quantum is as good or only slightly worse than classical models. A depiction of a hybrid network from the Qiskit texbook is below. 

![layers](https://github.com/JoshR220/HC59_Final_Project/blob/main/images/layers_qiskit.png)

The greatest difference between the classical and quantum machine learning components is the computation of gradients for backpropogation. Quantum circuits use the parameter shift rule in order to calculate gradients. The Qiskit textbook shows the gradient rule as below. 
