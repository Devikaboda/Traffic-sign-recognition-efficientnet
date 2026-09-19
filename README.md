# Traffic Sign Recognition Using EfficientNet-B0

Traffic sign classification using **EfficientNet-B0** and the **German Traffic Sign Recognition Benchmark (GTSRB)** dataset.

## 📌 Project Overview

The goal of this project is to automatically recognize and classify traffic signs from images. This type of system can be useful in **driver-assistance systems and autonomous driving applications**.

The project uses **EfficientNet-B0**, a convolutional neural network pretrained on ImageNet, and applies transfer learning and fine-tuning for traffic sign classification.

## 🎯 Objective

- Classify traffic signs into **43 different classes**
- Build a deep learning image classification model using EfficientNet-B0
- Apply transfer learning and fine-tuning
- Evaluate the model using accuracy, precision, recall, F1-score, and a confusion matrix

## 📊 Dataset

The project uses the **GTSRB (German Traffic Sign Recognition Benchmark)** dataset.

- Training images: **39,209**
- Test images: **12,630**
- Number of classes: **43**
- Image size used for training: **64 × 64**
- Training/validation split: **80:20**
### 🔗 Dataset

The GTSRB dataset is publicly available on Kaggle:

[**GTSRB - German Traffic Sign Recognition Benchmark**](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign)

## 🧠 Model Architecture

The model is based on **EfficientNet-B0** with ImageNet pretrained weights.

The classification head consists of:

**EfficientNet-B0**  
↓  
**Global Average Pooling**  
↓  
**Dropout (0.3)**  
↓  
**Dense Layer (43 classes)**  
↓  
**Softmax**



## 🔄 Training Approach

The model was trained in two stages using transfer learning.

### Stage 1 — Transfer Learning

- EfficientNet-B0 ImageNet pretrained weights were used.
- The EfficientNet-B0 base model was frozen.
- Only the newly added classification layers were trained.
- Learning rate: `0.001`
- Epochs: `5`
- Batch size: `32`

### Stage 2 — Fine-Tuning

- The EfficientNet-B0 base model was unfrozen.
- Batch Normalization layers were kept frozen for stable training.
- A smaller learning rate was used.
- Learning rate: `0.0001`
- Epochs: `5`

## 📈 Model Performance

The model was evaluated on **12,630 unseen test images**.

### Test Results

| Metric | Result |
|---|---:|
| Test Accuracy | **94.68%** |
| Macro Precision | **93%** |
| Macro Recall | **93%** |
| Macro F1-Score | **93%** |
| Weighted Precision | **95%** |
| Weighted Recall | **95%** |
| Weighted F1-Score | **95%** |

The final model achieved **94.68% accuracy on the test dataset**.

## 📊 Training Performance

The notebook contains the following visualizations:

- Training and Validation Accuracy
- Training and Validation Loss
- Confusion Matrix

These visualizations are available directly in the project notebook.

## 📊 Evaluation

The model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

The confusion matrix was used to identify traffic sign classes that were more frequently confused with each other.

## 🖼️ Sample Prediction

A sample test image was given to the trained model.

**Predicted Class:** Speed limit (30km/h)  
**Actual Class:** Speed limit (30km/h)  
**Confidence:** 99.99%

The prediction matched the actual class for this sample.

## 🛠️ Technologies Used

- **Python**
- **TensorFlow / Keras**
- **EfficientNet-B0**
- **NumPy**
- **Pandas**
- **Scikit-learn**
- **Matplotlib**
- **GTSRB Dataset**
- **Kaggle**

## 📁 Project Structure

```
Traffic-sign-recognition-efficientnet/
│
├── README.md
├── traffic-sign-recognition-efficientnet-b0-project.ipynb
└── .gitignore

```
## ▶️ How to Run

1. Open the notebook in **Kaggle** or another Python environment.
2. Add the GTSRB dataset.
3. Update the dataset path if required.
4. Run the notebook cells in order.
5. The model will be trained using transfer learning and fine-tuning.
6. Evaluate the model using the test dataset.

## 🔍 Key Features

- Classification of **43 traffic sign categories**
- EfficientNet-B0 transfer learning
- Two-stage training strategy
- Fine-tuning of the pretrained network
- Stratified training/validation split
- Confusion matrix-based error analysis
- Individual image prediction

## 🚀 Future Improvements

- Apply data augmentation to improve generalization.
- Experiment with higher input resolutions.
- Investigate frequently confused traffic sign classes.
- Compare EfficientNet-B0 with other deep learning architectures.
- Deploy the trained model for real-time traffic sign recognition.

## 📌 Conclusion

This project demonstrates the use of **transfer learning and fine-tuning with EfficientNet-B0** for traffic sign classification.

The trained model achieved **94.68% accuracy on 12,630 unseen GTSRB test images**, demonstrating its ability to classify traffic signs across 43 categories.

The project also includes classification metrics, a confusion matrix, training performance graphs, and sample predictions for evaluating the model.

## 👩‍💻 Author

**Devika Boda**

B.Tech Computer Science Engineering

