# 😷 Mask Detection System  

This project implements a **Mask Detection System** using **Machine Learning**. The system detects whether a person is wearing a mask, offering a practical solution for public safety in various environments. 🌍  

---

## ✨ Features  
- 🟢 **Real-time mask detection** with high accuracy.  
- 🧠 Utilizes a **pre-trained ResNet50 model**, fine-tuned for this task.  
- 📊 Handles large-scale datasets with efficient preprocessing and batch processing.  
- ⚡ Compatible with Google Colab for training and inference.  
- 🔍 Robust performance in diverse lighting and positioning conditions.  

---

## 💻 Technologies Used  
- 🐍 **Python**  
- 🔗 **TensorFlow**  
- ⚙️ **Keras**  
- 📊 **NumPy**  
- 🧹 **Pandas**  
- 📈 **Matplotlib**  
- ☁️ **Google Colab**  

---

## 📁 Dataset  
The system processes a dataset of **40,000 images**:  
1. 🖼️ Images are resized to **512x512 resolution** for memory efficiency.  
2. 🔄 Data generators are used for seamless batch processing.  

---

## 🛠️ Installation  

### 📥 Clone the Repository  
```bash  
git clone https://github.com/Himanshu20752005/mask-detection-system.git  
cd mask-detection-system


---

## 🚀 USAGE
--------
1. **Preprocess the dataset:**
```python
from tensorflow.keras.preprocessing.image import ImageDataGenerator

train_datagen = ImageDataGenerator(rescale=1./255, rotation_range=20, zoom_range=0.2, horizontal_flip=True)
train_generator = train_datagen.flow_from_directory('./dataset/train', target_size=(512, 512), batch_size=32, class_mode='binary')

