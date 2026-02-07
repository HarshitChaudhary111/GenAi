# 🎨 GAN-Based MNIST Digit Generation

This lab project implements a **Generative Adversarial Network (GAN)** using PyTorch to generate handwritten digits from the MNIST dataset. The project demonstrates how a Generator and Discriminator compete during training to produce realistic synthetic images.

The model trains on MNIST images, generates samples at different epochs, saves final generated digits, and evaluates outputs using a simple classifier. The full workflow follows the implementation shown in the lab notebook .

---

# 📌 Features

* GAN implementation from scratch using PyTorch
* Generator & Discriminator neural networks
* MNIST handwritten digit generation
* Real-time sample saving during training
* Final image generation after training
* Visualization of training progress
* Basic classifier for evaluation

---
---

# ⚙️ Technologies Used

* Python
* PyTorch
* Torchvision
* Matplotlib
* PIL

---

# 🧾 Dataset

**MNIST Handwritten Digit Dataset**

* Grayscale Images
* Image Size: 28 × 28
* Automatically downloaded using torchvision

Images are normalized to the range [-1, 1] during preprocessing.

---

# 🏗️ Model Architecture

## 🔹 Generator

Input:

* Random noise vector (size = 100)

Layers:

* Linear → ReLU
* Linear → ReLU
* Linear → ReLU
* Linear → Tanh

Output:

* Generated 28×28 image

---

## 🔹 Discriminator

Input:

* Flattened 28×28 image

Layers:

* Linear → LeakyReLU
* Linear → LeakyReLU
* Linear → Sigmoid

Output:

* Probability of real or fake image

---

# 🚀 Training Details

| Parameter       | Value                |
| --------------- | -------------------- |
| Epochs          | 60                   |
| Batch Size      | 64                   |
| Noise Dimension | 100                  |
| Learning Rate   | 0.0002               |
| Optimizer       | Adam                 |
| Loss Function   | Binary Cross Entropy |

The discriminator learns to distinguish real vs fake images, while the generator learns to fool the discriminator.

---

# 📊 Training Process

During training:

* Generator creates fake images from random noise.
* Discriminator compares real and fake images.
* Loss values (D_loss and G_loss) are printed every epoch.
* Sample images are saved every 5 epochs.

Example outputs and training logs are shown in the lab results .

---

# 🖼️ Generated Results

According to the visualization grid on page 6, image quality improves significantly from early epochs (5,10) to later epochs (40,50), showing clearer digit shapes .
<img width="1116" height="700" alt="Screenshot 2026-02-07 224314" src="https://github.com/user-attachments/assets/c4e2a3f1-e235-47d9-bc2e-4b9088829880" />

---

# 🧪 Classifier Evaluation

A simple MNIST classifier is trained to evaluate generated images:

* Linear neural network
* CrossEntropyLoss
* Generated images are converted from:

  * Range [-1,1] → [0,1]
  * 1 channel → 3 channels
  * Resized to 224×224

This helps assess how realistic the generated digits are.

---
---

# 🧠 Key Learnings

* GAN training involves adversarial learning between two networks.
* Generator improves by learning discriminator feedback.
* Image quality improves progressively with epochs.
* Balance between Generator and Discriminator losses is important.

---

# 📈 Future Improvements

* Use DCGAN (Convolutional GAN)
* Add TensorBoard visualization
* Improve Generator architecture
* Train on CIFAR-10 or Fashion-MNIST

---

# 👨‍💻 Author

**Harshit Chaudhary**
Bennett University
Generative AI Lab Project
