# Quantum vs Classical Machine Learning on Iris Dataset

This repository contains an educational exploration of binary classification using both Quantum Machine Learning (QML) with PennyLane and classical machine learning with scikit-learn. We use the well-known Iris dataset (Setosa vs. Versicolor) to compare model performance, pipeline design, and code structure.

## 🔧 Technologies Used

- Python 3.x
- [PennyLane](https://pennylane.ai/)
- PyTorch
- Scikit-learn
- NumPy

## 📊 Dataset

We use the Iris dataset provided by scikit-learn. It contains 3 classes:
- Setosa (0)
- Versicolor (1)
- Virginica (2)

For this experiment, we only use two classes (Setosa vs. Versicolor) to keep the quantum circuit small and simple.

## 🚀 Pipeline Overview

### 1. Data Preprocessing
- Load the Iris dataset
- Filter for Setosa and Versicolor classes only
- Normalize features using `StandardScaler`
- Select 2 features for the quantum model
- Convert data into PyTorch tensors (for QML)

### 2. Classical ML
- Use Logistic Regression from scikit-learn
- Train and evaluate model on the same data split

### 3. Quantum ML
- Use 2-qubit quantum circuit built with PennyLane
- Encode data with RX gates
- Add entanglement using CNOT
- Apply trainable RY gates
- Measure expectation value of PauliZ
- Train using PyTorch optimizer and BCELoss

### 4. Comparison
- Accuracy of both models is printed at the end
- QML may be slightly lower but shows promising performance

## ✅ Example Output
```
Epoch 5: Loss = 0.5301
Epoch 10: Loss = 0.3842
...
Classical Logistic Regression Accuracy: 0.9500
Quantum Classifier Accuracy: 0.9000
```

## 💡 Notes
- Quantum models are limited by the number of qubits (we use 2 here)
- This is a toy example to understand the workflow, not to outperform classical models
- Real advantage of QML may come in higher-dimensional, more complex datasets

## 📚 References
- PennyLane Docs: https://docs.pennylane.ai
- QML Course: https://pennylane.ai/qml/course/
- Scikit-learn: https://scikit-learn.org

## ✨ Future Work
- Try multiclass classification
- Use more features (4) with amplitude encoding
- Run on real quantum hardware (IBM Q, Amazon Braket, etc)
- Explore other QML models: variational circuits, quantum SVMs, etc

---

Made with ❤️ for learning and exploration.

