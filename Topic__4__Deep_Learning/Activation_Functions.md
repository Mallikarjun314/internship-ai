# Important Activation Functions

\
\
\
\
\
\

## 1. Sigmoid (Logistic) ⭐

**Formula**:

$$
\sigma(x) = \frac{1}{1 + e^{-x}}
$$

* **Range**: (0, 1)
* **Use case**: Output layer for binary classification
* **Drawbacks**: Vanishing gradients, not zero-centered

\
\
\
\
\
\


## 2. Tanh (Hyperbolic Tangent) ⭐

**Formula**:

$$
\tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}
$$

* **Range**: (–1, 1)
* **Use case**: Hidden layers (better than sigmoid)
* **Drawbacks**: Still suffers from vanishing gradients

\
\
\
\
\
\


## 3. ReLU (Rectified Linear Unit) ⭐

**Formula**:

$$
f(x) = \max(0, x)
$$

* **Range**: \[0, ∞)
* **Use case**: Default for hidden layers in most modern networks
* **Pros**: Sparse activation, computationally efficient
* **Drawbacks**: Dying ReLU (neurons can get stuck at zero)

\
\
\
\
\
\

## 4. Leaky ReLU

**Formula**:

$$
f(x) = 
\begin{cases}
x, & \text{if } x > 0 \\
\alpha x, & \text{otherwise}
\end{cases}
\quad \text{(typically } \alpha = 0.01\text{)}
$$

* **Range**: (–∞, ∞)
* **Use case**: Fixes dying ReLU problem
* **Pros**: Allows small gradient when input < 0

\
\
\
\
\
\


## 5. Parametric ReLU (PReLU)

* Same as Leaky ReLU, but the slope $\alpha$ is **learned** during training.

\
\
\
\
\
\

## 6. ELU (Exponential Linear Unit)

**Formula**:

$$
f(x) = 
\begin{cases}
x, & \text{if } x > 0 \\
\alpha(e^x - 1), & \text{if } x \le 0
\end{cases}
$$

* **Pros**: Zero-centered, smooth
* **Better than** ReLU in some cases

\
\
\
\
\
\

## 7. SELU (Scaled Exponential Linear Unit)

* A scaled version of ELU used in **self-normalizing neural networks**.
* Only works well with **specific initializations and architecture constraints**.

\
\
\
\
\
\

## 8. Swish

**Formula**:

$$
f(x) = x \cdot \sigma(x)
$$

* **Proposed by**: Google Brain
* **Pros**: Smooth, non-monotonic
* **Performs better** than ReLU on deeper networks

\
\
\
\
\
\

## 9. Mish

**Formula**:

$$
f(x) = x \cdot \tanh(\ln(1 + e^x)) = x \cdot \tanh(\text{softplus}(x))
$$

* **Pros**: Smooth, better empirical results than Swish and ReLU in some cases
* **Drawback**: More computationally expensive

\
\
\
\
\
\

## 10. Softmax ⭐

**Formula**:

$$
\sigma(z_i) = \frac{e^{z_i}}{\sum_j e^{z_j}}
$$

* **Use case**: Output layer for **multi-class classification**
* **Converts raw scores into probabilities**

\
\
\
\
\
\

### Summary Table:

| Name       | Output Range | Zero-Centered | Vanishing Gradient | Used In               |
| ---------- | ------------ | ------------- | ------------------ | --------------------- |
| Sigmoid    | (0, 1)       | ❌             | ✅                  | Binary output layer   |
| Tanh       | (–1, 1)      | ✅             | ✅                  | Legacy models         |
| ReLU       | \[0, ∞)      | ❌             | ❌ (mostly)         | Most hidden layers    |
| Leaky ReLU | (–∞, ∞)      | ✅ (partial)   | ❌                  | Improved ReLU         |
| PReLU      | (–∞, ∞)      | ✅             | ❌                  | Learnable Leaky       |
| ELU        | (–α, ∞)      | ✅             | ❌                  | Alternative to ReLU   |
| SELU       | (–∞, ∞)      | ✅             | ❌                  | Self-normalizing nets |
| Swish      | (–∞, ∞)      | ✅             | ❌                  | Deep networks         |
| Mish       | (–∞, ∞)      | ✅             | ❌                  | Newer networks        |
| Softmax    | (0, 1)       | ❌             | ❌                  | Multi-class output    |


Would you like a visual diagram or code snippets for each function (in PyTorch or TensorFlow)?
