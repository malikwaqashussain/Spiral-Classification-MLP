# Spiral Classification with Multilayer Perceptron (MLP)

This project involves designing, training, and evaluating a **Multilayer Perceptron (MLP)** to classify a challenging **3-class spiral dataset**. The dataset is synthetically generated to present complex, non-linear decision boundaries, making it an ideal candidate for testing deep learning models.

## Project Objective

To build and tune an MLP that can effectively classify data points in a 3-class spiral distribution, despite noise and overlapping regions.

---

## Dataset

The dataset was generated using a custom spiral generator function:
- **Points per class:** 200  
- **Number of classes:** 3  
- **Noise level:** 0.4

Each point lies on a spiral arm corresponding to its class, introducing complexity that requires non-linear decision boundaries.

---

## Model Architecture

The MLP model was built using **PyTorch**, with the following architecture:

- **Input layer:** 2 neurons (x, y coordinates)
- **Hidden Layer 1:** 128 neurons, ReLU activation
- **Hidden Layer 2:** 64 neurons, ReLU activation
- **Output Layer:** 3 neurons (softmax via `CrossEntropyLoss`)

**Optimizer:** Adam  
**Learning Rate:** 0.01  
**Epochs:** 500  
**Batch Size:** 32  

---

## Training and Evaluation

- Training/validation split: **80/20**
- Training was conducted for 500 epochs with real-time tracking of:
  - **Loss**
  - **Accuracy**
- Final metrics were visualized using plots for:
  - Loss curves
  - Accuracy curves
  - Decision boundary visualization

---

## Results

- The MLP successfully learned non-linear patterns in the spiral dataset.
- The decision boundary closely follows the class spirals, indicating strong performance.
- Some overfitting was observed and mitigated through architectural tuning.

---

## Key Learnings

- **Model Depth:** Two hidden layers provided sufficient learning capacity without overfitting.
- **Learning Rate:** Critical to convergence—`0.01` performed best.
- **Overfitting Control:** Avoided through proper layer sizing and early evaluations.
- **Further Improvements:**
  - Add **Dropout** or **Batch Normalization**
  - Experiment with **learning rate schedules**
  - Use **advanced activations** (e.g., GELU)
