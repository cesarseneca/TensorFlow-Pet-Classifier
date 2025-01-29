# 🐶🐱 TensorFlow Pet Classifier  

Welcome to **TensorFlow Pet Classifier**! 🎯 This project uses **Convolutional Neural Networks (CNNs)** to classify images of **dogs** and **cats** from a dataset.  

## 📸 Example Prediction  
The model analyzes images and predicts whether the image belongs to a **dog 🐶** or a **cat 🐱** with an estimated probability.  

![alt text](image.png)

---

## 🚀 Features 

✅ **CNN model based on VGG16 / MobileNetV2 / ResNet**  
✅ **Training with `tf.keras` and `ImageDataGenerator`**  
✅ **Data augmentation to improve accuracy**  
✅ **Callbacks: `EarlyStopping`, `ReduceLROnPlateau`, and `ModelCheckpoint`**  
✅ **Model evaluation with performance metrics and result visualization**  
✅ **Prediction of images in a grid of 10 random samples** 

## 🏗️ Project Structure 
```
TensorFlow-Pet-Classifier/
├── data/                  # Training and test data
│   ├── train/             # Training images
│   │   ├── cat/           # Cat images
│   │   └── dog/           # Dog images
│   └── test/              # Test images
├── src/                   # Source code
│   └── explore.ipynb      # Notebook to explore and train the model
├── models/                # Trained models
├── requirements.txt       # Project dependencies
└── README.md              # This file
```
## 🧠 Technical Details 

### 🏋️ Training  
A **pretrained CNN** with transfer learning is trained on a dataset of **22,030 training images** and **12,500 validation images**.  

**Parameters:**  
- Optimizer: `Adam`
- Learning Rate: `0.001` (dynamically adjusted with `ReduceLROnPlateau`)
- Loss: `Binary Crossentropy`
- Epochs: `10`
- Batch Size: `32`
- Data Augmentation (`ImageDataGenerator`):  
  - Rotation, translation, zoom, and horizontal flip  

### 📊 **Metrics**  
- **Model accuracy**: `~85%` on validation  
- **Loss and accuracy curves**

## ⚠️ **Limitations**  
There is a **limitation with the test folder** where the test images should be properly structured and should only contain images, as the model may fail to perform if additional files are present. It is essential to ensure that the test set contains only valid image files (e.g., `.jpg`, `.png`) to avoid errors during evaluation.

## 📜 **License**  
This project is distributed under the MIT License.
