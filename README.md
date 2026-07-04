# 🤟 ASL Alphabet Classifier

A Convolutional Neural Network (CNN) based image classifier that recognizes American Sign Language (ASL) alphabet hand signs, deployed as an interactive Streamlit web app.

🔗 **Live Demo:** [Hugging Face Spaces](https://huggingface.co/spaces/sanzayjana/asl-sign-language-interpreter)

---

## 📌 Overview

This project trains a CNN to classify images of hand signs into ASL alphabet letters (A–Z, plus `space`, `del`, and `nothing`). The trained model is served through a Streamlit interface where users can upload an image and instantly get a prediction.

## 📊 Results

| Metric | Score |
|---|---|
| Training Accuracy | 98.4% |
| Validation Accuracy | 80.7% |
| Epochs | 5 |

## 🗂️ Dataset

[ASL Alphabet Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet) from Kaggle — contains thousands of labeled images across 29 classes (A–Z, space, delete, nothing).

## 🏗️ Project Structure

```
asl-sign-language-interpreter/
│
├── train_model.py        # CNN training script
├── app.py                 # Streamlit inference app
├── requirements.txt       # Python dependencies
├── class_labels.txt       # Generated after training
├── asl_model.h5            # Trained model (generated after training)
└── README.md
```

## ⚙️ Tech Stack

- **Python**
- **TensorFlow / Keras** — CNN model building & training
- **Streamlit** — web app interface
- **Hugging Face Spaces** — deployment

## 🚀 How to Run Locally

1. Clone the repo
```bash
git clone https://github.com/sanzayjanarthanan/asl-sign-language-interpreter.git
cd asl-sign-language-interpreter
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. (Optional) Train the model — download the Kaggle dataset first and place it in `data/asl_alphabet_train/`
```bash
python train_model.py
```

4. Run the Streamlit app
```bash
streamlit run app.py
```

## 🧠 Model Architecture

A sequential CNN with:
- 3 Convolutional + MaxPooling blocks (32 → 64 → 128 filters)
- Dense layer (256 units) with Dropout for regularization
- Softmax output layer over 29 classes

## 📸 Demo

Upload a hand sign image → get the predicted letter with confidence score and top-3 alternative predictions.

## 👤 Author

**Sanjay** — CSE student, Anna University
Connect on [LinkedIn](#) | [GitHub](https://github.com/sanzayjanarthanan)

## 📄 License

This project is open source and available under the MIT License.

