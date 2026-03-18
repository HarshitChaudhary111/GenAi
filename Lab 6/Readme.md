# 🎨 GenAI Lab-6 — Pix2Pix (Edge → Image Translation)

This lab project implements **Image-to-Image Translation using Pix2Pix GAN**, where the model learns to convert edge images into realistic shoe images.

Additionally, a **CNN baseline model** is implemented to compare performance with the GAN approach.

The implementation follows the workflow shown in the lab notebook .

---

## ✨ Features

* Pix2Pix GAN implementation using PyTorch
* U-Net Generator with skip connections
* PatchGAN Discriminator
* Edge → Shoe image translation
* CNN baseline model for comparison
* Visualization of outputs (Input vs Pix2Pix vs CNN)

---


## ⚙️ Technologies Used

* Python
* PyTorch
* Torchvision
* NumPy
* Matplotlib
* PIL

---

## 🧾 Dataset

* **Edges2Shoes Dataset**
* Each image contains:

  * Left → Edge image
  * Right → Real shoe image

Dataset is split during loading into:

```
Edge Image → Input  
Real Image → Target
```

---

## 🧠 Model Architecture

---

## 🔹 Generator (U-Net)

* Encoder: Downsampling using Conv layers
* Decoder: Upsampling using ConvTranspose
* Skip connections for better detail preservation

```
Input (Edge Image)
   ↓
Encoder (Downsampling)
   ↓
Bottleneck
   ↓
Decoder (Upsampling + Skip Connections)
   ↓
Output (Generated Image)
```

---

## 🔹 Discriminator (PatchGAN)

* Takes both edge and real/generated image
* Classifies image patches as real or fake
* Helps generate sharper images

---

## 🔹 CNN Baseline

* Simple encoder-decoder CNN
* No adversarial training
* Used for comparison with GAN output

---

## 📉 Loss Functions

### Generator Loss

```
Adversarial Loss + 100 × L1 Loss
```

### Discriminator Loss

```
Real Loss + Fake Loss
```

### CNN Loss

```
L1 Loss
```

---

## 🚀 Training Details

| Parameter     | Value  |
| ------------- | ------ |
| Epochs (GAN)  | 5      |
| Epochs (CNN)  | 3      |
| Batch Size    | 4      |
| Learning Rate | 0.0002 |
| Optimizer     | Adam   |

---

## 🖼️ Results

The output visualization includes:

* Input Edge Image
* Pix2Pix Generated Image
* CNN Generated Image

📌 Observation:

* Pix2Pix produces more realistic and detailed outputs
* CNN outputs are blurrier and less sharp

(Final comparison visualization shown on page 5 of the lab results .)

---


## 🧠 Key Learnings

* GANs can generate realistic images using adversarial training
* U-Net improves image translation with skip connections
* PatchGAN focuses on local image quality
* GANs outperform simple CNNs in image generation tasks

---

## 📈 Future Improvements

* Train for more epochs for better results
* Use larger batch size
* Try other datasets (maps, facades)
* Add evaluation metrics like SSIM or PSNR

---

## 👨‍💻 Author

**Harshit Chaudhary**
Bennett University
Generative AI Lab Project

