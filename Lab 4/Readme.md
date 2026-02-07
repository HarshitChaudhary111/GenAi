<h1 align="center">GenAI Lab-4 — Advanced Text Generation (N-Gram • RNN • Transformer)</h1>

<p align="center">
Next-Word Prediction and Text Generation using Statistical NLP, RNNs, and Transformer Architecture
</p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3.10-blue"/>
<img src="https://img.shields.io/badge/TensorFlow-Keras-orange"/>
<img src="https://img.shields.io/badge/NLP-Text%20Generation-green"/>
<img src="https://img.shields.io/badge/Gradio-UI-purple"/>
<img src="https://img.shields.io/badge/Status-Completed-success"/>
</p>

---

# 📖 Overview

This project is part of **Generative AI Lab-4**, where multiple NLP models are implemented to generate text from a custom AI-related dataset.

The lab progresses through three major approaches:

✅ N-Gram Statistical Language Model
✅ RNN Neural Text Generator
✅ Transformer-Based Text Generator

The goal is to understand how language models evolve from simple probability-based prediction to modern attention-based architectures.

---

# 🧠 What This Project Demonstrates

* Tokenization and Sequence Generation
* Next Word Prediction Training
* Sequential Modeling using RNN
* Self-Attention using Transformer Blocks
* Positional Encoding
* Interactive Text Generation UI using Gradio

---

# 🏗️ Model Architecture

---

## 🔹 N-Gram Model

Basic probabilistic approach:

* Predicts next word using previous word
* Uses dictionary mapping
* No deep learning

### ⚠️ Limitations

* Short context memory
* Repetitive outputs
* No semantic understanding

---

## 🔹 RNN Text Generation

Neural network architecture:

```
Embedding → SimpleRNN → Dense Softmax
```

Key Features:

* Learns sequence patterns
* Better coherence than N-Gram
* 100 Training Epochs

---

## 🔹 Transformer Text Generator

Modern NLP architecture:

```
Embedding
   ↓
Positional Encoding
   ↓
Multi-Head Attention
   ↓
Feed Forward Network
   ↓
Softmax Prediction
```

Key Concepts:

* Self Attention
* Layer Normalization
* Context Awareness
* Parallel Processing

---

# 📊 Model Comparison

| Model       | Type            | Context Understanding | Output Quality |
| ----------- | --------------- | --------------------- | -------------- |
| N-Gram      | Statistical     |  Low                 | ⭐ Basic        |
| RNN         | Deep Learning   |  Medium              | ⭐⭐ Better      |
| Transformer | Attention-Based |  High                | ⭐⭐⭐ Advanced   |

---

# 🖥️ Interactive UI

This project includes **Gradio interfaces**:

### 🟣 RNN Text Generation UI

* Enter Seed Text
* Select Word Length
* Generate AI Text
<img width="900" height="625" alt="Screenshot 2026-02-05 155633" src="https://github.com/user-attachments/assets/3ff3a1a1-17f5-4427-a01e-3ce4e326e274" />

### 🔵 Transformer Text Generation UI

* Advanced attention-based generation
* Interactive web interface
<img width="900" height="622" alt="Screenshot 2026-02-07 232651" src="https://github.com/user-attachments/assets/364a2aa5-91fd-4cce-a755-746dbb69a565" />

---

---

# 📈 Results & Observations

✔️ N-Gram generates local word predictions only
✔️ RNN learns sentence flow and produces meaningful sequences
✔️ Transformer achieves strongest contextual understanding and smoother generation

Training logs show accuracy increasing significantly across epochs, indicating successful learning.

---

# 🎯 Key Learnings

* Traditional NLP vs Deep Learning Language Models
* Sequence Modeling
* Self Attention Mechanism
* Transformer Architecture Fundamentals
* Building AI Text Generation UI

---

# 🔮 Future Improvements

* Replace SimpleRNN with LSTM/GRU
* Add Temperature Sampling
* Train on Large Dataset
* Deploy UI to HuggingFace Spaces

---

# 👨‍💻 Author

**Harshit Chaudhary**
Bennett University
Generative AI • Deep Learning

---

<p align="center">
⭐ If you like this project, consider starring the repo!
</p>

