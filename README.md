# Amazon Reviews Sentiment Analysis  

<p align="center">
  <img src="https://raw.githubusercontent.com/Kaancnkya/amazon_reviews_sentiment/main/gradio_ui_1.png" width="45%" alt="Positive Prediction" />
  <img src="https://raw.githubusercontent.com/Kaancnkya/amazon_reviews_sentiment/main/gradio_ui_2.png" width="45%" alt="Negative Prediction" />
</p>

A complete sentiment analysis pipeline built using **TensorFlow**, **TextVectorization**, **custom preprocessing**, and a **Gradio UI** for real-time predictions. Developed entirely in Google Colab.

A complete sentiment analysis pipeline built using **TensorFlow**, **TextVectorization**, **custom preprocessing**, and a **Gradio UI** for real-time predictions. Developed entirely in Google Colab.

---

## Project Overview  
This project performs sentiment classification (Positive / Negative) on Amazon review texts.  
The workflow includes:

- Loading and cleaning the dataset  
- Removing noise (punctuation, symbols, numbers)
- Applying a short-review filter (removing reviews under 3 words)
- Vectorizing text using TensorFlow's **TextVectorization** layer
- Training a deep learning model (LSTM / Dense architecture)
- Saving the vectorizer + model pipeline
- Deploying a **Gradio** interface for real-time classification

The notebook used for this project can be found here:  
🔗 **[amazon_reviews.ipynb](amazon_reviews.ipynb)**

---

## 1. Data Cleaning Pipeline

Custom cleaning function applied to each review:

- Lowercasing  
- Regex-based noise removal  
- Removing special chars  
- Normalizing whitespace  
- Removing very short reviews (<3 tokens)

This ensures higher-quality training data and avoids unstable vectorization.

---

## 🔢 2. Text Vectorization (TensorFlow)

Used TensorFlow's `TextVectorization` layer:

- `max_tokens = 20,000`
- `sequence_length = 200`
- Output mode: `int`

Vectorizer is adapted on the cleaned text column.

This creates an indexed vocabulary and fixed-length integer sequences for the neural network.

---

## 3. Model Architecture

A simple but effective deep learning model:

- **Embedding Layer**
- **LSTM / RNN / Dense stack**
- **Sigmoid output** (binary classification)

Model was trained on the transformed sequences and achieved stable predictions.

---

## 4. Gradio UI for Real-Time Predictions

A custom Gradio interface was built to demo the model:

<p align="center">
  <img src="https://raw.githubusercontent.com/Kaancnkya/amazon_reviews_sentiment/main/gradio_ui_1.png" width="45%" alt="Positive Prediction" />
  <img src="https://raw.githubusercontent.com/Kaancnkya/amazon_reviews_sentiment/main/gradio_ui_2.png" width="45%" alt="Negative Prediction" />
</p>

Users can type any review text and instantly see the predicted sentiment.

---

## 5. Example Predictions

| Review Text                          | Prediction |
|--------------------------------------|------------|
| “Amazing product, totally worth it!” | Positive   |
| “Terrible quality, waste of money.”  | Negative   |

---

## Repository Structure

amazon_reviews_sentiment/
│
├── amazon_reviews.ipynb        # Main project notebook
├── gradio_ui_1.png             # Positive prediction screenshot
├── gradio_ui_2.png             # Negative prediction screenshot
└── README.md                   # Project documentation

---

## Technologies Used

- Python  
- TensorFlow / Keras  
- TextVectorization Layer  
- Pandas / NumPy  
- Regular Expressions (Regex)
- Gradio (for UI)
- Google Colab

---

## Summary

This project demonstrates:

- Real-world NLP preprocessing  
- TensorFlow text pipelines  
- Deep learning classification  
- Clean end-to-end ML workflow  
- User-friendly deployment via Gradio  

Perfect for ML portfolios, job applications, or showcasing NLP skills.

---

## Author  
**Kaan Cankaya**  
Google Colab · TensorFlow · NLP · Machine Learning
