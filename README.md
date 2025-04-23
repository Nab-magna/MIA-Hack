# MIA-Hack

# 🧬 Cancer Classification with VGG16 on the MedMNIST Dataset

This project explores using deep learning — specifically, a VGG16-based architecture — to classify cancer types from medical images in the MedMNIST dataset. The idea is to leverage transfer learning to improve performance on small medical datasets.

---

## 📚 About the Dataset

We're using the **PathMNIST** subset from [MedMNIST](https://medmnist.com/), which contains histopathologic images of human tissue.

- **Image size:** 28x28 RGB
- **Classes:** 9 (including normal tissue and multiple cancer subtypes)
- **Use case:** Patch-level classification for cancer diagnosis

---

## 🔧 Approach

We're using **VGG16** (pretrained on ImageNet) as a feature extractor, then fine-tuning it for our 9-class classification task.

Key highlights:
- Input layer resized to accept 28x28x3 images
- Replaced top layers with custom Dense layers
- Trained with `Adam` optimizer and `categorical_crossentropy` loss

---

## 🛠 How to Run This

1. Clone this repository:
   ```bash
   git clone https://github.com/Nab-magna/MIA-Hack.git
   cd MIA-Hack
