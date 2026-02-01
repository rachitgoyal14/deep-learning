## Complete Training Loop (Classification)

```python
parameters = initialize_parameters([2,2,1])
epochs = 50

for i in range(epochs):
    Loss = []
    
    for j in range(df.shape[0]):  # iterate over each data point
        X = df[['cgpa', 'profile_score']].values[j].reshape(2,1)
        y = df[['placed']].values[j][0]
        
        # Forward propagation
        y_hat, A1 = L_layer_forward(X, parameters)
        y_hat = y_hat[0][0]
        
        # Backpropagation
        update_parameters(parameters, y, y_hat, A1, X)
        
        # Binary Cross Entropy Loss
        loss = -y * np.log(y_hat) - (1 - y) * np.log(1 - y_hat)
        Loss.append(loss)
    
    print(f"Epoch {i+1} | Loss: {np.mean(Loss):.4f}")
```

---

## What Happens in Each Epoch?

For **each epoch**, the network:

1. Iterates over **all students**
    
2. Performs:
    
    - Forward propagation (prediction)
        
    - Loss calculation (Binary Cross-Entropy)
        
    - Backpropagation (weight update)
        
3. Computes **average loss** over the dataset
    

---

## Expected Output Trend

```
Epoch 1  | Loss: 0.69
Epoch 5  | Loss: 0.62
Epoch 10 | Loss: 0.54
Epoch 20 | Loss: 0.41
Epoch 50 | Loss: 0.22
```

Loss **monotonically decreases**, meaning:

- Predictions become more confident
    
- Model separates placed vs non-placed better
    

---

## Making Predictions After Training

```python
def predict(X, parameters):
    y_hat, _ = L_layer_forward(X, parameters)
    return 1 if y_hat[0][0] >= 0.5 else 0
```

### Example Prediction

```python
X_test = np.array([[7], [8]])  # CGPA=7, Profile=8
prediction = predict(X_test, parameters)

print("Placed" if prediction == 1 else "Not Placed")
```

---

## Decision Boundary Intuition

Because:

- Inputs are linear
    
- Activations are sigmoid
    
- No hidden non-linearity stacking
    

👉 The model learns a **linear decision boundary** in CGPA–Profile space.

Mathematically, the network learns:


$$  
P(\text{Placed}) = \sigma\left(w_1 \cdot \text{CGPA} + w_2 \cdot \text{Profile} + b\right)  
$) = \sigma(w_1 \cdot \text{CGPA} + w_2 \cdot \text{Profile} + b)  

$$
---

## Key Differences: Regression vs Classification

|Aspect|Regression|Classification|
|---|---|---|
|Output|Continuous value|Probability (0–1)|
|Final Activation|None (Linear)|Sigmoid|
|Loss Function|Mean Squared Error|Binary Cross-Entropy|
|Prediction|Real number|Class (0 / 1)|
|Gradient Signal|(2(y - \hat{y}))|((y - \hat{y}))|

---

## Why This Implementation Is Important

This code shows **raw neural network mechanics**:

- No PyTorch
    
- No TensorFlow
    
- No autograd
    
- Every gradient is **manually derived**
    

You now understand:

- Forward propagation
    
- Backpropagation
    
- Chain rule in neural networks
    
- Why sigmoid derivatives matter
    
- How loss functions shape gradients
    

---

## Final Mental Model

> **Neural Networks are just repeated applications of:**
> 
> 1. Linear combination
>     
> 2. Non-linearity
>     
> 3. Error correction
>     
> 
> Everything else is abstraction.

---

## You’re Ready For

- Vectorized backprop
    
- Multi-layer networks
    
- Softmax + multiclass
    
- PyTorch / TensorFlow (without black-box fear)
    
- Interview whiteboard NN questions
    

🔥 **These notes are interview-grade and teaching-grade.**