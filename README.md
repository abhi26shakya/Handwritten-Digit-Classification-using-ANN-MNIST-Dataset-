# ✍️ Handwritten Digit Classification using ANN (MNIST)

## 📌 Overview

This project implements a **Handwritten Digit Classification system** using an **Artificial Neural Network (ANN)** built with TensorFlow and Keras.

The model is trained on the **MNIST dataset**, which consists of grayscale images of handwritten digits (0–9), and predicts the correct digit with high accuracy.

---

## 🚀 Features

* Load and preprocess MNIST dataset
* Normalize pixel values (0–255 → 0–1)
* Build ANN model using Keras Sequential API
* Train model with validation monitoring
* Visualize:

  * Accuracy curves
  * Loss curves
* Evaluate model performance on test data

---

## 🧠 Tech Stack

* Python 🐍
* NumPy
* TensorFlow / Keras
* Matplotlib
* Scikit-learn

---

## 📂 Dataset

* Dataset: **MNIST (built-in Keras dataset)**
* 70,000 grayscale images of handwritten digits

  * 60,000 training images
  * 10,000 testing images
* Image size: **28 × 28 pixels**

---

## ⚙️ Project Workflow

### 1️⃣ Data Loading

```python
(X_train, y_train), (X_test, y_test) = keras.datasets.mnist.load_data()
```

---

### 2️⃣ Data Preprocessing

* Normalize pixel values:

```python
X_train = X_train / 255
X_test = X_test / 255
```

---

### 3️⃣ Model Architecture

* Flatten Layer (28×28 → 784)
* Hidden Layer (128 neurons, ReLU)
* Hidden Layer (32 neurons, ReLU)
* Output Layer (10 neurons, Softmax)

---

### 4️⃣ Model Compilation

* Loss: `sparse_categorical_crossentropy`
* Optimizer: `Adam`
* Metric: `Accuracy`

---

### 5️⃣ Model Training

* Epochs: 25
* Validation Split: 20%

---

### 6️⃣ Evaluation

* Accuracy score on test data
* Prediction using `argmax`
* Performance visualization

---

## 📊 Results

* Training Accuracy: ~99%
* Validation Accuracy: ~97–98%
* Test Accuracy: ~97%+

📌 The model performs well but shows slight **overfitting**, which is common for ANN on MNIST.

---

## 📈 Visualizations

### 🔹 Accuracy Graph

* Shows training vs validation accuracy over epochs


<img width="566" height="410" alt="Accuracy_graph" src="https://github.com/user-attachments/assets/1b7415fa-1e94-432e-bde9-9068c955bbe3" />


### 🔹 Loss Graph

* Shows training vs validation loss
* Helps detect overfitting


<img width="551" height="407" alt="Loss_graph" src="https://github.com/user-attachments/assets/1fd55c70-3db9-495a-a3a2-1a9d7afed8f1" />


## 📁 Project Structure

```
├── mnist_ann.ipynb
├── README.md
├── requirements.txt
```

---

## 🛠️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/your-username/mnist-ann-classifier.git

# Navigate to project folder
cd mnist-ann-classifier

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook
```

---

## 🎯 Future Improvements

* Add Dropout to reduce overfitting
* Use EarlyStopping
* Implement CNN for better accuracy (99%+)
* Hyperparameter tuning
* Deploy model using Streamlit

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork this repo and submit a pull request.

---

## 📜 License

This project is open-source and available under the MIT License.

---

## ⭐ Support

If you found this project helpful, give it a ⭐ on GitHub!
