# 🧠 Autoencoder vs Variational Autoencoder on CIFAR-10

This project demonstrates the implementation and comparison between a **Standard Autoencoder (AE)** and a **Variational Autoencoder (VAE)** using PyTorch on the CIFAR-10 dataset. The main objective is to understand how **KL Divergence** impacts reconstruction quality and latent space learning.

The models are trained, evaluated, and visually compared before and after applying KL divergence based on the deep learning lab workflow .

---

# 📌 Features

* Autoencoder without KL Divergence
* Variational Autoencoder with KL Diverence
* Reconstruction Visualization
* Loss & Accuracy Comparison
* Reparameterization Trick Implementation
* CIFAR-10 Dataset Training

---

# ⚙️ Technologies Used

* Python
* PyTorch
* Torchvision
* Matplotlib
* Pandas

---

# 🧾 Dataset

**CIFAR-10 Dataset**

* 32x32 RGB Images
* 10 Image Classes
* Automatically downloaded using torchvision

---

# 🏗️ Model Architecture

## 🔹 Autoencoder (Without KL Divergence)

### Encoder

* Linear (3072 → 512)
* Linear (512 → 128)

### Decoder

* Linear (128 → 512)
* Linear (512 → 3072)

### Loss Function

```
MSE Loss
```

---

## 🔹 Variational Autoencoder (With KL Divergence)

### Encoder Outputs

* Mean (μ)
* Log Variance (logσ²)

### Reparameterization Trick

```
z = μ + ε * σ
```

### Loss Function

```
Total Loss = Reconstruction Loss + KL Divergence
```

---

# 🚀 Training Details

| Model       | Epochs | Optimizer | Learning Rate |
| ----------- | ------ | --------- | ------------- |
| Autoencoder | 10     | Adam      | 1e-3          |
| VAE         | 15     | Adam      | 1e-3          |

---

# 📊 Results

| Model           | Reconstruction Loss | Reconstruction Accuracy (%) |
| --------------- | ------------------- | --------------------------- |
| Without KL (AE) | 0.009040            | 99.09%                      |
| With KL (VAE)   | 0.061961            | 93.80%                      |

👉 Autoencoder achieves higher reconstruction accuracy, while VAE improves latent space structure and generative capability.

---

# 🖼️ Reconstruction Comparison

## Before KL Divergence (Autoencoder)

* Sharper reconstructions
* Lower loss values

## After KL Divergence (VAE)

* Slightly blurrier outputs
* Better probabilistic representation

---

# 🧠 Key Learnings

* Autoencoders focus mainly on reconstruction accuracy.
* VAEs introduce probabilistic learning using KL divergence.
* KL divergence regularizes the latent space for better generative modeling.

---

# 📈 Future Improvements

* Implement Convolutional Autoencoders
* Latent Space Visualization (t-SNE / PCA)
* Hyperparameter Tuning
* Train for More Epochs

---

# 👨‍💻 Author

**Harshit Chaudhary**
Bennett University
Generative AI / Deep Learning Lab

