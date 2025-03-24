# CNN-LungCancerClassifier

## Project Overview

This project aims to develop a deep learning model to classify medical lung scans into two types of cancer: Adenocarcinoma and Squamous Cell Carcinoma. Convolutional Neural Networks (CNNs) were employed to achieve this objective. Diverse experiments were conducted with different model architectures and hyperparameters to optimize accuracy and minimize loss.

## Dataset

The dataset used in this project is the [Lung-PET-CT-DX dataset](https://www.cancerimagingarchive.net/collection/lung-pet-ct-dx/), containing over 250,000 lung scans from 355 subjects. For the scope of this project, we utilized 20,000 images from the Adenocarcinoma (A) and Squamous Cell Carcinoma (G) classes, ensuring a balanced distribution between both classes. The images were preprocessed and split into training (70%), validation (15%), and testing (15%) sets.

## Models

Two distinct models were tested:

Custom CNN Architecture (Baseline Model) 

Designed with: four 2D convolutional layers, four 2D max-pooling layers, a flatten layer, and a dense layer with 512 neurons. 

Total parameters: 59 million.

Transfer Learning with VGG16:

Pre-trained VGG16 model fine-tuned for lung cancer classification. The model includes twelve convolutional and five max-pooling layers. 

Total parameters: 82 million.

## Training Configuration

Optimizer: Adam

Loss Function: Binary Cross Entropy

Metrics: Accuracy and Validation Loss

Batch Size: 64

Early Stopping: Enabled with patience of 7 epochs

Epochs: 20 (VGG16), 30 (Baseline)

Hardware: v2-8 TPU on Google Colab

## Results

The VGG16 model slightly outperformed the baseline CNN model. Key results include:

- Validation Accuracy: 95.17% (VGG16), 93.90% (Baseline)

- Validation Loss: 0.1356 (VGG16), 0.2005 (Baseline)

- Test Accuracy: 95.03% (VGG16), 94.60% (Baseline)

- Test Loss: 0.1428 (VGG16), 0.2025 (Baseline)

## Challenges

The major challenges encountered were:

- Handling large datasets (over 100GB)

- Extensive training times (up to 10 hours for VGG16)

- Lack of domain knowledge in medicine and radiology

## Conclusion

The VGG16 model achieved state-of-the-art performance with 95% accuracy, demonstrating its robustness and generalization capability. Despite challenges, the project succeeded in delivering a highly accurate classification model.

## Acknowledgements

Special thanks to Professor Zoran Djordjevic and colleagues who supported the project.


