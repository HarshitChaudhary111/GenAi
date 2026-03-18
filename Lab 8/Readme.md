# 🎨 GenAI Lab-8 — DCGAN & Conditional GAN on CIFAR-10

This lab project implements a **Deep Convolutional GAN (DCGAN)** to generate images from noise using the CIFAR-10 dataset.
It also explores **latent space analysis** and extends the model to a **Conditional GAN (cGAN)** for controlled image generation.

The implementation follows the workflow shown in the lab notebook .

---

## ✨ Features

* DCGAN implementation using TensorFlow/Keras
* Image generation from random noise
* Latent space interpolation and visualization
* Stability testing (same noise → same output)
* Latent dimension variation experiments
* Conditional GAN (cGAN) for class-based generation


## ⚙️ Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib

---

## 🧾 Dataset

* **CIFAR-10 Dataset**
* Images normalized to range [-1, 1]
* Loaded using TensorFlow datasets

---

## 🧠 Model Architecture

---

## 🔹 Generator

* Input: Random noise vector (latent_dim = 100)
* Dense → Reshape → Conv2DTranspose layers
* Batch Normalization + LeakyReLU
* Output: 32×32×3 image

---

## 🔹 Discriminator

* Conv2D layers with LeakyReLU
* Dropout for regularization
* Final Dense layer for real/fake classification

---

## 📉 Loss Functions

```
Generator Loss → Binary Crossentropy (real labels for fake images)
Discriminator Loss → Real Loss + Fake Loss
```

---

## 🚀 Training Details

| Parameter        | Value       |
| ---------------- | ----------- |
| Epochs           | 20          |
| Batch Size       | 128         |
| Latent Dimension | 100         |
| Optimizer        | Adam (1e-4) |

Training completes successfully across all epochs as shown in logs (page 4) .

---

## 🖼️ Results

* Generated images from random noise
* Progressive improvement in image quality
* Diverse outputs from different latent vectors

📌 Observations:

* Different noise → different images
* Same noise → same output (model stability)
* Smooth transitions observed in interpolation

(Visual outputs shown in pages 5–8 of the lab results .)

---

## 🔍 Latent Space Analysis

### Interpolation

* Smooth transition between two images
* Demonstrates continuity of latent space

### Stability Test

* Same latent vector produces identical outputs

### Latent Dimension Variation

* Tested for 50, 100, 200
* Higher dimensions → more diversity

---

## 🔹 Conditional GAN (cGAN)

* Adds label input along with noise
* Uses embedding layer for class conditioning
* Enables controlled image generation

```
Input = Noise × Label Embedding
```


## 🧠 Key Learnings

* GANs learn to generate images from noise
* DCGAN improves stability using convolutional layers
* Latent space controls diversity and smooth transitions
* Conditional GAN enables class-specific generation

---

## 📈 Future Improvements

* Train for more epochs for sharper images
* Use larger image datasets
* Add evaluation metrics (FID Score)
* Improve architecture with StyleGAN

---

## 👨‍💻 Author

**Harshit Chaudhary**
Bennett University
Generative AI Lab Project
