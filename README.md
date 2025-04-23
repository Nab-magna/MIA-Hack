# MIA-Hack

# 🧬 Cancer Classification with VGG16 on the MedMNIST Dataset

This project explores using deep learning — specifically, a VGG16-based architecture — to classify cancer types from medical images in the MedMNIST dataset. The idea is to leverage transfer learning to improve performance on small medical datasets.

---

## 📚 Datasets Used

We're working with 4 datasets from [MedMNIST](https://medmnist.com/), a benchmark of standardized medical image tasks:

| Dataset         | Type             | Task                        | Classes |
|----------------|------------------|-----------------------------|---------|
| OCTMNIST        | Retinal (OCT)     | Binary (normal vs disease)  | 2       |
| PneumoniaMNIST  | Chest X-rays      | Binary (pneumonia vs normal)| 2       |
| RetinaMNIST     | Fundus images     | Multiclass (DR grading)     | 5       |
| BreastMNIST     | Ultrasound        | Binary (benign vs malignant)| 2       |

All images are standardized to 28×28 resolution and are grayscale or RGB depending on the dataset.

---

## 🔧 Approach

We're using **VGG16**, a pretrained convolutional neural network, and fine-tuning it to work with multiple MedMNIST datasets.

Each dataset is handled as a separate classification task, but the pipeline (preprocessing → feature extraction → classification) is kept consistent.

- Custom preprocessing for grayscale vs RGB handling
- Used `VGG16` as a feature extractor
- Final layers adjusted for binary or multiclass classification

---

## 🛠 How to Run This

1. Clone this repository:
   ```bash
   git clone https://github.com/Nab-magna/MIA-Hack.git
   cd MIA-Hack
