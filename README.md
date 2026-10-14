# 📩 SMS Spam Detection Using Deep Learning

## 📌 Project Overview

SMS Spam Detection is a deep learning project that automatically classifies text messages as **Spam** or **Ham (Not Spam)** using a Long Short-Term Memory (LSTM) neural network.

The project uses Natural Language Processing (NLP) techniques to preprocess SMS messages, convert text into numerical sequences, and train a deep learning model to identify potential spam messages.

## 🎯 Objectives

- Detect spam SMS messages automatically.
- Preprocess and clean text messages.
- Convert text into numerical sequences using tokenization and padding.
- Build and train an LSTM model using TensorFlow/Keras.
- Evaluate model performance using accuracy, precision, recall, and F1-score.
- Visualize results using a confusion matrix.
- Predict whether newly entered SMS messages are spam or legitimate.

## 🛠️ Technologies Used

- **Language:** Python
- **Platform:** Google Colab / Jupyter Notebook
- **Deep Learning:** TensorFlow, Keras
- **Data Processing:** Pandas, NumPy
- **Natural Language Processing:** Keras Tokenizer
- **Machine Learning Evaluation:** Scikit-learn
- **Visualization:** Matplotlib, Seaborn

## 📂 Dataset

The project uses the SMS Spam Collection dataset, containing labelled SMS messages.

- `ham` — legitimate messages
- `spam` — unwanted or potentially fraudulent messages

The uploaded dataset contains 5,572 rows before preprocessing. This project uses a manageable subset of approximately 2,000 labelled messages for experimentation.

**Dataset columns:**
- `v1` — message label
- `v2` — SMS message text

## ⚙️ Project Workflow

1. **Data Loading:** Load the SMS dataset using Pandas.
2. **Data Cleaning:** Handle missing values, remove duplicate messages, and normalize text.
3. **Label Encoding:** Convert `ham` to `0` and `spam` to `1`.
4. **Tokenization:** Convert SMS words into numerical tokens.
5. **Padding:** Make input sequences a fixed length.
6. **Model Building:** Create an LSTM neural network with embedding, dropout, and dense layers.
7. **Model Training:** Train the model using labelled SMS messages.
8. **Model Evaluation:** Calculate accuracy, precision, recall, and F1-score.
9. **Visualization:** Display training graphs and the confusion matrix.
10. **Spam Prediction:** Test the trained model on new SMS messages.

## 🧠 Why LSTM?

Long Short-Term Memory (LSTM) is a type of recurrent neural network designed to learn sequential patterns in data.

It is suitable for SMS classification because the order and context of words can help distinguish legitimate messages from spam. The embedding layer learns word representations, and the LSTM processes the resulting sequence before the final classification layer predicts the spam probability.

## 🏗️ Model Architecture

The neural network contains the following layers:

1. **Embedding Layer:** Converts token IDs into dense vector representations.
2. **LSTM Layer:** Learns sequential patterns in SMS text.
3. **Dropout Layer:** Helps reduce overfitting.
4. **Dense Layer:** Learns additional classification features.
5. **Output Layer:** Uses sigmoid activation to produce a spam probability.

The model uses the Adam optimizer and binary cross-entropy loss.

## 📊 Evaluation Metrics

The model is evaluated using:

- **Accuracy:** Measures the proportion of correctly classified messages.
- **Precision:** Measures how many predicted spam messages are actually spam.
- **Recall:** Measures how many actual spam messages are correctly detected.
- **F1-score:** Combines precision and recall into a single metric.
- **Confusion Matrix:** Shows correct and incorrect predictions for both classes.

*Actual evaluation scores should be added after running the notebook.*

## 💻 Sample Prediction

**Input:**
```text
Congratulations! You have won a free prize. Claim now!
```

**Illustrative output:**
```text
Prediction: SPAM
Spam probability: Model-dependent
```

**Input:**
```text
Hi, are we meeting at college tomorrow?
```

**Illustrative output:**
```text
Prediction: HAM (NOT SPAM)
Spam probability: Model-dependent
```

The predictions depend on the trained model and are not guaranteed to be correct.

## 🚀 How to Run the Project

### Step 1: Open Google Colab

Visit [Google Colab](https://colab.research.google.com/) and create a new notebook.

### Step 2: Upload the Dataset

Upload `spam_sms.csv` using the Colab file upload feature.

### Step 3: Install Dependencies

Run the following command if the libraries are not already installed:

```python
!pip install tensorflow pandas numpy scikit-learn matplotlib seaborn
```

### Step 4: Execute the Notebook

Run the notebook cells in order to:

- Load and preprocess the dataset.
- Tokenize and pad SMS messages.
- Build and train the LSTM model.
- Evaluate the model.
- Display the confusion matrix.
- Predict new SMS messages.

### Step 5: Test a New Message

Use the prediction function to enter an SMS message and obtain its classification.

## 📁 Suggested Repository Structure

```text
SMS-Spam-Detection/
│
├── README.md
├── spam_sms.csv
├── SMS_Spam_Detection.ipynb
├── sms_spam_lstm.keras
└── sms_tokenizer.pkl
```

The notebook contains the preprocessing, training, evaluation, and prediction code. The model and tokenizer files are generated after training.

**Note:** Upload the notebook and dataset if permitted by the dataset's licence. Model and tokenizer files are optional because they can be regenerated by running the notebook.

## 🔮 Future Enhancements

- Develop a web application for real-time SMS classification.
- Create a user-friendly interface to enter messages.
- Compare LSTM with Simple RNN and GRU models.
- Improve performance through hyperparameter tuning.
- Explore larger datasets and additional text preprocessing methods.
- Integrate the model into a mobile application.

## ✅ Conclusion

This project demonstrates how deep learning and Natural Language Processing can be used to classify SMS messages as spam or legitimate. By applying text preprocessing, tokenization, sequence padding, and LSTM-based classification, the system provides a practical foundation for automated SMS spam detection.

## 👨‍💻 Project Information

**Project Title:** SMS Spam Detection Using Deep Learning

**Domain:** Deep Learning and Natural Language Processing (NLP)

**Model:** Long Short-Term Memory (LSTM)

**Framework:** TensorFlow/Keras
