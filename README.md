Here is the `README.md` content in plaintext for you to copy:

# 🕵️‍♂️ AI vs Real Image Detector

This project is a Binary Image Classifier capable of distinguishing between **Real Photographs** and **AI-Generated Images** (e.g., Midjourney, Stable Diffusion).

It achieves **\~86% accuracy** using Transfer Learning on the **MobileNetV2** CNN architecture.

## 🚀 Features

  * **Lightweight Model:** Uses MobileNetV2 for fast inference, even on CPUs.

  * **Web Interface:** Includes a **Gradio** app (`app.py`) to drag-and-drop images for testing.

  * **Tunable Sensitivity:** The UI features a slider to adjust the detection threshold, helping to catch subtle AI fakes.

  * **Training Script:** Complete, readable code (`train_model.py`) to train your own version on custom datasets.

## 🛠️ Installation

1.  **Clone the repository:**

    ```
    git clone https://github.com/Jaisev-Sachdev/ai-detector.git
    cd ai-image-detector

    ```

2.  **Install dependencies:**

    ```
    pip install -r requirements.txt

    ```

3.  **Run the Web App:**

    ```
    python app.py

    ```

## 📊 Dataset

Trained on a balanced dataset of **\~30,000 Real** and **\~30,000 AI** images.
*(Note: The dataset itself is not included in this repo due to size constraints).*

## 🧠 Model Architecture

  * **Base:** MobileNetV2 (Pre-trained on ImageNet)

  * **Head:** GlobalAveragePooling2D -\> Dropout(0.2) -\> Dense(1, Sigmoid)

  * **Loss Function:** Binary Crossentropy

  * **Optimizer:** Adam (lr=0.0001)
