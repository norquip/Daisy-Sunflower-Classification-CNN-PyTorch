

#  Daisy vs Sunflower Classification (CNN - PyTorch)

This project implements a Convolutional Neural Network (CNN) in PyTorch to classify images of daisies and sunflowers.

##  Objective

To design and train a deep learning model capable of distinguishing between flower classes using image data.

---

##  Model Architecture

The network consists of four convolutional blocks:

- Conv2d layers (3 → 32 → 64 → 128 → 256 channels)  
- ReLU activation  
- MaxPool2d for spatial downsampling  
- BatchNorm2d for stable and faster training  

### Classifier

- AdaptiveAvgPool2d → reduces feature maps to 1×1  
- Flatten → converts to feature vector  
- Linear → ReLU → BatchNorm1d → Dropout(0.4)  
- Final Linear layer → class scores  

---

##  Approach

- Built a preprocessing pipeline using PyTorch transformations  
- Used PIL for image handling  
- Implemented DataLoader for batching and efficient training  
- Split data into training, validation, and test sets  

---

##  Results

- Achieved high classification performance (~97–98% accuracy)  
- Adam optimizer outperformed SGD  
- Learning rate significantly affected training stability  

---

##  Key Insights

- Data transformations help reduce misclassification  
- High learning rates cause instability in training  
- Adam optimization provides better convergence than SGD  
- Class imbalance introduces additional challenges in model performance  

---

##  Tools

- Python  
- PyTorch  
- PIL  
- DataLoader / torchvision  

---

##  Dataset

Subset of the TensorFlow flower dataset (daisy & sunflower classes):  
https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz

---

## 📌 Notes

This project was inspired by deep learning coursework but implemented and analyzed independently.
