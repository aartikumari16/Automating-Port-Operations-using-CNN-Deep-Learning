# Automating Port Operations using CNN & Deep Learning

This showcases an end-to-end implementation of deep learning models aimed at automating port operations through boat image classification. The primary goal is to build efficient models—one from scratch and another lightweight variant leveraging transfer learning—for deployment in mobile environments.

---

##  Project Overview

**Objectives:**
1. **Built a CNN network** from scratch to classify different types of boats from images.
2. **Developed a lightweight model** using transfer learning (MobileNetV2) to enable mobile-friendly deployment.
3. Evaluated the performance differences and learning efficiency between both approaches.

---

##  Repository Contents

- `Automating_Port_Operations.ipynb` – Jupyter notebook containing the complete implementation, training pipeline, evaluation metrics, and performance plots.
- `README.md` – This project overview.

---

##  Model Details

### 1. CNN from Scratch
- **Architecture**: Classic CNN built using Keras (Conv2D → MaxPooling → Conv2D → MaxPooling → GlobalAveragePooling → Dense layers → Softmax output).
- **Training**:
  - Data split ~80:20 (train vs test), with validation via `ImageDataGenerator` or `image_dataset_from_directory`.
  - Normalization: image rescaling (`1./255`).
  - Compiled using Adam optimizer, categorical cross-entropy loss, tracking accuracy, precision, and recall.
- **Evaluation**: Includes loss/accuracy plots, test evaluation, confusion matrix heatmap, and classification report.

### 2. Transfer Learning with MobileNetV2
- **Architecture Highlights**:
  - MobileNetV2 as base feature extractor.
  - Added: GlobalAveragePooling, Dropout, Dense + BatchNormalization layers, ending in a softmax output layer.
- **Training**:
  - Data split ~70:30 (train vs test), with validation split.
  - Same preprocessing pipeline as above.
  - Compiled with Adam optimizer and categorical cross-entropy; monitored accuracy, precision, recall.
  - Training runs for ~50 epochs with early stopping on validation loss.
- **Evaluation**: Includes training vs validation loss and accuracy plots, plus final test performance.

---

##  Evaluation & Observations

Compare both models based on:
- Accuracy, precision, recall
- Training time and resource usage
- Overfitting tendencies
- Suitability for deployment (model size, inference speed)

Discuss trade-offs: e.g., higher accuracy vs efficiency, training complexity vs adaptability.

---


##  Author & Contributions

- **Author**: [aartikumari16](https://github.com/aartikumari16)
- See `Automating_Port_Operations.ipynb` for detailed commentary.

---

Happy exploring and feel free to suggest enhancements!  
