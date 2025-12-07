# ai-detector
A deep learning model using MobileNetV2 to detect AI-generated images vs real photos. Includes a Python training script and a Gradio web interface for testing.

This project is a Binary Image Classifier capable of distinguishing between **Real Photographs** and **AI-Generated Images** (e.g., Midjourney, Stable Diffusion).

It achieves **~80% accuracy** using Transfer Learning on the **MobileNetV2** CNN architecture.

## 🚀 Features
* **Lightweight Model:** Uses MobileNetV2 for fast inference, even on CPUs.
* **Web Interface:** Includes a `Gradio` app (`app.py`) to drag-and-drop images for testing.
* **Tunable Sensitivity:** The UI features a slider to adjust the detection threshold, helping to catch subtle AI fakes.
* **Training Script:** Complete, readable code (`train_model.py`) to train your own version on custom datasets.

## 🛠️ Installation
1.  Clone the repository:
    ```bash
    git clone [https://github.com/Jaisev-Sachdev/ai-detector]
    cd ai-image-detector
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the Web App:
    ```bash
    python app.py
    ```

## 📊 Dataset
Trained on a balanced dataset of ~30,000 Real and ~30,000 AI images. (Dataset not included in this repo due to size).

## 🧠 Model Architecture
* **Base:** MobileNetV2 (Pre-trained on ImageNet)
* **Head:** GlobalAveragePooling2D -> Dropout(0.2) -> Dense(1, Sigmoid)
* **Loss Function:** Binary Crossentropy
* **Optimizer:** Adam (lr=0.0001)
