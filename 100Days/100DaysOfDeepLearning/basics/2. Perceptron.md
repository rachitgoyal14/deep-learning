### What is a Perceptron?

Perceptron is an algorithm used for `supervised machine learning`. It is like any other algorithm such as linear regression, just that it is designed in such a way that it automatically became a building block of deep learning.

It can also be interpreted as a `mathematical model/function`.

![[Pasted image 20260102150129.png]]


Let's have a look at a more formal image:
![[Pasted image 20260102150253.png]]


If you have a look at the image below, the perceptron is similar to an actual biological neuron. 
![[Pasted image 20260102151141.png]]
Both of them may seem similar but they here are the differences:
1. **Complexity**: Neurons are very complex relative to perceptrons
2. **Nucleus**: Nucleus is sort of a black box in a neuron but in a perceptron, we are aware that summation and the step function is happening in the neuron of a perceptron.
3. **Neuroplasticity**: Dendrites' thickness changes over time whereas the connections remain consistent in a perceptron.

### Geometric Intuition of a Perceptron

![[Pasted image 20260102152319.png]]


![[Pasted image 20260102152438.png]]
If you look at the equation `z = ax + by + c`, it is the equation of a straight line.

`ax + by + c >= 0` represents a region, and vice versa.

Perceptron is nothing but a line which creates two regions and divides the data into 2 different classes. This is why perceptron is also known as a **binary classifier**.

> LIMITATION
> Perceptron can only classify linear or sort of linear data. 
> If we have a completely non-linear dataset, then perceptron will fail.

