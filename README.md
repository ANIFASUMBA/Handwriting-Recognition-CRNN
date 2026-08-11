# Handwritten Character & Word Recognition (CNN + CRNN)
This repository contains a two-phase deep learning project built with PyTorch that transitions from single-character classification to full-word sequence recognition. It features interactive desktop canvas applications built with `tkinter`, allowing you to test the models live with your own mouse drawings.
---
## 🚀 Features & Project Structure.

### 1. Single-Character Recognition (`CNN`)
* **Dataset:** Trained on the EMNIST (Balanced) dataset
* **Architecture:** Traditional Convolutional Neural Network (CNN) featuring conv layers, max-pooling, and dropout for regularization.
* **Interactive App:** `canvas_app.py` allows you to draw single letters (`A-Z`) or digits (`0-9`) on a $280\times280$ canvas for real-time inference.
  
### 2. Full-Word Sequence Recognition (`CRNN` + `CTC Loss`)

* **Dataset:** Trained on dynamically generated synthetic text images with heavy data augmentations (random slants, perspective shifts, and Gaussian blurs) to simulate human handwriting imperfections.
* **Architecture:** Convolutional Recurrent Neural Network (CRNN). Uses a deeper CNN with Batch Normalization to extract visual slices, a Bidirectional LSTM to process spatial sequences, and Connectionist Temporal Classification (CTC) Loss to decode arbitrary string alignments without explicit segmentation.
* **Interactive App:** `word_canvas_app.py` features an elongated canvas allowing you to write complete words out of the trained vocabulary pool (e.g., `CAT`, `DOG`, `FOX`, `BOX`, `HOME`, `WORK`).

---
## 🛠️ Tech Stack & Dependencies
* **Language:** Python
* **Deep Learning Framework:** PyTorch & Torchvision
* **GUI Framework:** Tkinter (Python Standard Library)
* **Image Processing:** OpenCV (`opencv-python`), Pillow (`PIL`), and NumPy

To install the necessary external dependencies, run:
```bash
pip install torch torchvision numpy opencv-python Pillow
