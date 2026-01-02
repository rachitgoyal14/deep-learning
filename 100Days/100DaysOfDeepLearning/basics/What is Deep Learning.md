###### Introduction
Deep Learning is a subfield of Artificial Intelligence and Machine Learning that is inspired by the structure of a human brain.

Deep Learning algorithms attempt to draw similar conclusions as humans would by continually analyzing data with a given logical structure called '**Neural Network**'.

###### How does it differ from Machine Learning?
Deep Learning is a subset of Machine Learning where the relation of input and output is decided through a logical structure called a **neural network** whereas in machine learning, it usually statistical analysis.

There are a few more differences:
1. **Dataset Requirement**:  Deep Learning models requires a lot more data than Machine Learning models.
![[Pasted image 20260102143048.png]]
	If you analyze the graph, after a certain amount of data, the performance of the machine learning model stagnates whereas the deep learning model's performance keeps on improving.
	Hence, Deep Learning is `data hungry`.
2. **Hardware Requirements**: Training any deep learning model requires GPU because of complex matrix multiplication whereas ML models require only CPU. 
	1. **Training Time**: DL has much more training time, sometimes days or even weeks whereas ML has much lower training time, longest one lasting hours.
3. **Feature Selection**: DL algorithms use `Representation Learning` which extracts the features themselves from the dataset whereas ML algorithms require the engineering of feature extraction.
4. **Interpretability/Explainability**: 
   **DL models' outputs are not explainable**.
   What does it mean? => DL Models just churn out the output but their working is like a `black-box` where we have no understanding of why it did what it did. 
   For example, if I train a classification model that classifies an image as a dog or a cat, we do not know what it did internally to gives us that specific result.
   In contrast, **ML models have high explainability** such  decision trees. 
###### Neural Networks
These are logical structure trying to replicate `human brains` to relate the input and output.
There are a few different kinds of neural networks:
1. ANN
2. CNN = for image generation
3. RNN = for speech/text
4. GAN = generate (text) image

###### Why is Deep Learning getting mainstream now?
1. Applicability
2. Performance 

###### Definition
Deep Learning is part of a broader family of machine learning methods based on artificial neural networks with representation learning.
Deep Learning Algorithms uses multiple layers to progressively extract higher level features from the raw input. 
For Example, in image processing, lower layers may identify edges, while higher layers may identify the concepts relevant to a human such as digits or letters or faces.

###### Dog OR Cat Classification Problem
While classifying an image of an animal as a `dog` or a `cat`, 
	**Machine Learning**: I have to engineer the feature of classification of dog or a cat
	**Deep Learning**: It automatically engineers the features from the data input.


