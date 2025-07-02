# 🖥️ CNN From Scratch — MNIST Digit Classifier

This project implements a **Convolutional Neural Network (CNN)** from scratch in pure **Python** using only **NumPy** and **Matplotlib** — no external deep learning frameworks like TensorFlow or PyTorch. The network is trained on the **MNIST handwritten digit dataset** to classify images of digits from `0-9`.

---

## 📊 Project Highlights

- Custom implementation of **2D and 3D Convolution layers**, **ReLU activation**, **Max Pooling**, and **Softmax classifier**.
- Manual **forward propagation** and **backpropagation** with explicit gradient calculations and weight updates.
- Achieved **~80% test accuracy** using a simple 2-layer CNN architecture on a subset of MNIST.

---

## 📝 Tech Stack

- **Python 3**
- **NumPy**
- **Matplotlib**
- **TensorFlow Keras (only for MNIST data loading)**

---

## 📌 CNN Architecture

| Layer                      | Output Shape       | Description                                |
|:---------------------------|:------------------|:-------------------------------------------|
| Input                       | `28 x 28`          | Grayscale digit image                     |
| Conv2D (9 filters)          | `26 x 26 x 9`      | 9 learnable 3×3 filters                   |
| ReLU                        | `26 x 26 x 9`      | Activation function                       |
| MaxPool (2×2)               | `13 x 13 x 9`      | Downsamples by taking max in 2×2 regions  |
| Conv3D (10 filters, depth 9)| `11 x 11 x 10`     | 10 learnable 3×3×9 filters                |
| ReLU                        | `11 x 11 x 10`     | Activation function                       |
| MaxPool (2×2)               | `5 x 5 x 10`       | Downsamples again                         |
| Flatten                     | `250`              | Converts to 1D vector                     |
| Softmax                     | `10`               | Output probability distribution (0-9)    |

---

## 🚀 How It Works

### 📥 Data Preprocessing
- MNIST images loaded via `tensorflow.keras.datasets`
- Pixel values normalized to range `[-0.5, 0.5]`

### ⚙️ Forward Propagation
- Each image passes through convolution, ReLU, and max pooling layers.
- Softmax produces a probability distribution over 10 classes.

### 📉 Loss Function
- Uses **Negative Log Likelihood (Cross-Entropy)** for classification.

### 🔄 Backpropagation
- Gradients computed manually for each layer using the chain rule.
- Weights and biases updated via gradient descent.

---

## 📊 Results

- Achieved **~90% test accuracy** after a few epochs on a small subset of the MNIST dataset (1000 training images).
- Visualized random test images with predicted and actual labels in a grid format.

---

## 📸 Sample Output

<img width="698" alt="Screenshot 2025-07-01 at 9 53 48 PM" src="https://github.com/user-attachments/assets/2c8d92e3-b201-4227-853d-91e1f50d0673" />




