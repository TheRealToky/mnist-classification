# MNIST Handwritten Digit Classification

A neural network built **from scratch** using only NumPy to classify handwritten digits from the [MNIST dataset](http://yann.lecun.com/exdb/mnist/). No deep learning frameworks — just pure math and backpropagation.

## 🧠 Architecture

| Layer      | Details                        |
|------------|--------------------------------|
| **Input**  | 784 neurons (28×28 flattened)  |
| **Hidden** | 10 neurons, ReLU activation    |
| **Output** | 10 neurons, Softmax activation |

- **Weight Initialization**: He initialization (`np.sqrt(2/n)`)
- **Optimizer**: Vanilla gradient descent
- **Learning Rate**: `0.01`
- **Iterations**: `5,000`

## 📊 Results

| Metric             | Value    |
|--------------------|----------|
| Training Accuracy  | ~90.6%   |
| Test Accuracy      | **90.89%** |

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- pip

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/TheRealToky/mnist-classification.git
   cd mnist-classification
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # macOS/Linux
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install numpy idx2numpy pandas matplotlib
   ```

4. **Download the MNIST dataset**

   Place the following files inside the `data/` directory:
   - `train-images.idx3-ubyte`
   - `train-labels.idx1-ubyte`
   - `t10k-images.idx3-ubyte`
   - `t10k-labels.idx1-ubyte`

   You can download them from the [official MNIST page](http://yann.lecun.com/exdb/mnist/).

5. **Run the notebook**
   ```bash
   jupyter notebook exploration.ipynb
   ```

## 📁 Project Structure

```
mnist-classification/
├── data/                    # MNIST dataset files (not tracked by git)
├── exploration.ipynb        # Main notebook — training, evaluation & inference
├── .env                     # Environment variables (e.g. Kaggle API key)
├── .gitignore
└── README.md
```

## 🔧 Key Functions

| Function               | Description                                          |
|------------------------|------------------------------------------------------|
| `init_params()`        | Initializes weights and biases with He initialization |
| `forward_propagation()`| Computes forward pass through the network             |
| `back_propagation()`   | Computes gradients via backpropagation                |
| `gradient_descent()`   | Runs the training loop for N iterations               |
| `test_model()`         | Evaluates accuracy on the test set                    |
| `inference()`          | Predicts a single image and displays the result       |

## 📝 License

This project is open source and available for learning purposes.
