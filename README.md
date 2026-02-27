# Neural Network from Scratch using NumPy (Regression)

An end-to-end implementation of a fully connected neural network built entirely from first principles using NumPy.

This project demonstrates a complete mathematical derivation and vectorised implementation of forward propagation, backpropagation, and gradient descent optimisation without relying on deep learning frameworks such as TensorFlow, PyTorch, Keras, or scikit-learn.

---

## Project Objective

To build and train a single-hidden-layer neural network for a regression task while understanding and implementing:

- The mathematical foundations of neural networks
- Chain rule-based backpropagation
- Vectorised gradient computation
- Model optimisation via gradient descent
- Hyperparameter tuning and performance evaluation

The model is applied to the Advertising dataset to predict product sales based on:

- TV advertising budget
- Radio advertising budget
- Newspaper advertising budget

---

## Neural Network Architecture

- Input Layer: 3 features
- Hidden Layer: H neurons (Sigmoid activation)
- Output Layer: 1 neuron (Linear activation)
- Loss Function: Mean Squared Error (MSE)

Mathematically:

Forward pass:
- z¹ = XW¹ᵀ + b¹ᵀ  
- a¹ = σ(z¹)  
- z² = a¹W² + b²  
- ŷ = z²  

Loss:
L = (1 / 2N) Σ (y − ŷ)²

Backpropagation gradients are derived analytically and implemented in fully vectorised form.

---

## Key Features

- Manual train–test split (80/20)
- Feature standardisation using training statistics only
- Fully vectorised forward and backward propagation
- Analytical gradient derivation
- Gradient descent optimisation
- Hyperparameter tuning:
  - Hidden units: {2, 4, 8, 16, 32}
  - Learning rates: {0.2, 0.3}
- Learning curve visualisation (training vs test loss)
- Reproducibility via fixed random seed

---

## Results

- Optimal number of hidden units selected via validation performance
- Optimal learning rate selected via systematic comparison
- Stable convergence observed through loss curves
- Demonstrates the bias–variance tradeoff via model capacity variation

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib

No deep learning libraries were used.

---

## Why This Project Matters

Modern machine learning frameworks abstract away the mathematical foundations of neural networks.  
This implementation focuses on understanding:

- How gradients are computed
- How parameters are updated
- How architecture affects performance
- How optimisation behaves during training

This project demonstrates strong fundamentals in machine learning and numerical computing.

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/yourusername/neural-network-from-scratch-numpy.git
cd neural-network-from-scratch-numpy
```

Install dependencies:

```bash
pip install numpy pandas matplotlib
```

Run the script:

```bash
python neural_network_from_scratch.py
```

---

## Future Improvements

- Add multiple hidden layers (deep network)
- Implement different activation functions (ReLU, Tanh)
- Add L2 regularisation
- Compare with scikit-learn's MLPRegressor
- Implement mini-batch gradient descent
- Add performance metrics (R², MAE)

---

## Author

Your Name  
