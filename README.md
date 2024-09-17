# MobileNet - A Case Study (Deep Learning Midterm Assignment)

## Introduction
MobileNets are lightweight models designed for efficient use on mobile and embedded devices, addressing the need for models that are small, fast, and accurate. This case study explores the architecture and application of MobileNets in image classification tasks.

## Group Members
- An Minh Tri (BI12-447)
- Nguyen Son (BI12-389)
- Nguyen Cong Quoc (BI12-375)
- Tran Ngoc Hai (BI12-150)
- Pham Trung Hieu (BI12-159)
- Tang Minh Tri (BI12-445)

## Dataset
### CIFAR-10 Dataset
- Contains 60,000 32x32 color images divided into 10 classes.
- 50,000 training images and 10,000 test images.
- Each class has 6,000 images.
![image](https://github.com/user-attachments/assets/1e55e108-4104-43ac-8afe-8a46e3a6f5ea)

### Data Preparation
- Images are normalized to a range of 0 to 1.
- One-hot encoding applied to target labels.

## Model Architecture
### Depthwise Separable Convolutions
MobileNets utilize Depthwise Separable Convolutions to reduce the number of parameters and computational requirements. This architecture consists of two steps:
1. **Depthwise Convolution**: Applies filters independently to each input channel.
![image](https://github.com/user-attachments/assets/77673861-4640-4c18-a707-88eb04bcebf0)
2. **Pointwise Convolution**: Uses 1x1 convolutions to mix the outputs.
![image](https://github.com/user-attachments/assets/1835259e-9341-4b61-b22b-fc54dc50c4ac)


### Input and Output
- **Input Layer**: 32x32x3 (RGB Image)
- **Output Layer**: 10 classes with softmax activation for multi-class classification.

## Evaluation
### Metrics
- **Test Loss**: Measures the average error between predicted and true labels using cross-entropy loss.
- **Test Accuracy**: Proportion of correctly predicted samples.

### Performance
- Our trained-from-scratch model achieved a test accuracy of approximately 71.58%.
- The pretrained MobileNet model achieved a test accuracy of about 73.26%.
- ![image](https://github.com/user-attachments/assets/b884e501-38a8-4148-9410-148c4837100d)

## Demo
The following demonstration showcases image classification using the two MobileNet models that we’ve trained to predict the contents of an input image.
![image](https://github.com/user-attachments/assets/6ced6918-00fa-4a78-8058-29f9e921a468)

For more details, please refer to the [full report](https://github.com/Xernnn/MobileNet-Classification/blob/main/MobileNet_for_image_classification.pdf).
