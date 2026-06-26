# How a Machine Learns (Neural Networks) — Notes

> **Source:** `transcriptions/08-how-machine-learns.md`
> **Module:** 04-ai-development-workflow

---

## Summary

This optional lesson explains the foundational mechanics of how neural networks learn: the forward pass (weighted sum → activation function → predicted output), loss measurement, backpropagation to adjust weights, and gradient descent to determine how to update weights and when to stop. It distinguishes parameters (learned during training) from hyperparameters (set before training) and covers common activation functions, cost functions, and the role of the learning rate.

---

## Key Concepts

### Artificial Neural Network (ANN) Structure

An ANN has three layer types: **input layer**, one or more **hidden layers**, and an **output layer**. Each layer contains nodes (neurons); connections between nodes have **weights**. DNNs, CNNs, RNNs, and LLMs all derive from this basic ANN structure.

### The Learning Process (7 Steps)

1. **Weighted sum**: multiply each input by its weight and sum — `z = w1*x1 + w2*x2 + bias`.
2. **Apply activation function** to the hidden layer's weighted sum — introduces non-linearity.
3. **Weighted sum for output layer** — same process through subsequent layers.
4. **Apply activation function to output layer** — can differ from hidden layer activation.
5. **Calculate cost/loss function** — measures difference between predicted ŷ and actual y.
6. **Backpropagation** — if difference is significant, adjust weights and biases.
7. **Iterate** — repeat one full pass (one **epoch**) until cost function stops decreasing.

### Why Activation Functions are Necessary

Without activation functions, stacking layers produces only a linear combination of inputs (no matter how many layers). Linear models can't solve complex, non-linear problems. Activation functions inject non-linearity, enabling the network to learn complex patterns.

### Common Activation Functions

| Function | Range | Use case |
|---|---|---|
| ReLU | [0, ∞) | Default for hidden layers; turns negative inputs to 0 |
| Sigmoid | (0, 1) | Binary classification and logistic regression |
| Tanh | (-1, 1) | Shifted sigmoid; used in hidden layers |
| Softmax | (0, 1) summing to 1 | Multi-class classification — output is a probability distribution |

- **Sigmoid** = binary (spam/not spam); **Softmax** = multi-class (cat/dog/bird).
- Different layers can use different activation functions (e.g., ReLU in hidden layers, Softmax in output layer).

### Cost Functions

- **Loss function**: measures error for a single training example.
- **Cost function**: measures average error across the entire training set.
- **MSE (Mean Squared Error)**: for regression problems.
- **Cross-entropy**: for classification problems; measures difference between predicted probability and actual label distribution.

### Gradient Descent

The optimization strategy that finds weights minimizing the cost function — like walking down a hill to find the lowest point:
- **Direction**: determined by the derivative of the cost function (negative derivative = go right, positive = go left).
- **Step size = learning rate** (hyperparameter set before training):
  - Too small: training takes very long.
  - Too large: oscillates, may not converge.
  - Just right: reaches the minimum efficiently.

### Parameters vs. Hyperparameters

| Type | Examples | Who sets it |
|---|---|---|
| Parameters | weights, biases | Machine learns these during training |
| Hyperparameters | number of layers, neurons, activation functions, learning rate, epochs | Human sets these before training |

AutoML automates hyperparameter selection — this is one of its primary advantages.

---

## Google Cloud Products & Tools Mentioned

| Product / Tool | What it does in this context |
|---|---|
| AutoML (Vertex AI) | Automatically selects hyperparameters, removing the need for manual experimentation |

---

## Exam Tips

- **Sigmoid** = binary classification; **Softmax** = multi-class classification — this distinction appears frequently.
- **Parameters** (weights, biases) = learned by machine; **hyperparameters** (learning rate, epochs, layers) = set by humans before training.
- **Learning rate** is a hyperparameter — controls how fast weights update (step size in gradient descent).
- One complete pass through all training data = one **epoch**.
- **ReLU** is the most common activation for hidden layers — outputs 0 for negative inputs, passes positive inputs unchanged.
- **Backpropagation** adjusts weights after each forward pass based on the cost function error.
- **Gradient descent** finds the cost minimum by following the negative gradient direction.
- MSE = regression; cross-entropy = classification — know which cost function goes with which problem type.

---

## Questions to Follow Up

- How does **dropout** (a regularization technique) fit into this learning framework — is it covered in the PMLE scope?
- Is the distinction between batch gradient descent, stochastic gradient descent, and mini-batch gradient descent testable on the PMLE exam?
