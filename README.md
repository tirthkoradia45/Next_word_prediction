# 🧠 Next Word Prediction using LSTM

An end-to-end Deep Learning project that predicts the **next word in a
sentence** using a Long Short-Term Memory (LSTM) neural network. The
trained model is integrated with a simple **Streamlit web application**
where users can enter text and receive a predicted next word.

## 🚀 Project Overview

Next Word Prediction is a Natural Language Processing (NLP) task where a
model learns patterns from text and predicts the most likely word that
comes next.

This project follows a complete workflow:

**Text Dataset → Text Preprocessing → Tokenization → Sequence Generation
→ LSTM Model → Model Training → Saved Model → Streamlit Application →
Next Word Prediction**

The repository contains the training notebooks, dataset, trained LSTM
model, tokenizer, sequence-length configuration, and Streamlit
application.

## ✨ Features

-   Predicts the next word from user-provided text
-   Uses an LSTM-based neural network
-   Uses Keras/TensorFlow for model loading and inference
-   Uses tokenization and sequence padding for text preprocessing
-   Provides an interactive Streamlit interface
-   Saves the trained model and preprocessing objects for reuse
-   Includes notebooks for model implementation and experimentation

## 🛠️ Tech Stack

  Technology           Purpose
  -------------------- ---------------------------------------------
  Python               Core programming language
  TensorFlow / Keras   LSTM model and inference
  NumPy                Numerical operations
  Streamlit            Interactive web application
  Pickle               Saving/loading tokenizer and configuration
  Jupyter Notebook     Model development and experimentation
  NLP                  Text preprocessing and next-word prediction

## 📂 Project Structure

``` text
Next_word_prediction/
│
├── app.py                    # Streamlit application
├── RNNimplementation.ipynb   # RNN/LSTM implementation and experimentation
├── codefile.ipynb            # Supporting code / experimentation
├── lstm_model (1).h5         # Trained LSTM model
├── tokenizer.pkl              # Saved text tokenizer
├── max_len.pkl               # Saved maximum sequence length
├── qoute_dataset.csv         # Text dataset used for training
└── README.md                 # Project documentation
```

## 🧠 How It Works

### 1. Text Tokenization

The input text is converted into numerical sequences using a trained
tokenizer.

For example:

``` text
"I love machine"
```

is converted into a sequence of token IDs.

### 2. Sequence Padding

The input sequence is padded to the required length so that it matches
the format expected by the trained model.

### 3. LSTM Prediction

The padded sequence is passed to the trained LSTM model.

The model produces probabilities for possible next words.

### 4. Select the Predicted Word

The word with the highest predicted probability is selected as the next
word.

``` text
Input:
"I love machine"

Prediction:
"learning"
```

## 🖥️ Streamlit Application

The Streamlit application is implemented in `app.py`.

It:

1.  Loads the trained LSTM model.
2.  Loads the tokenizer.
3.  Loads the saved maximum sequence length.
4.  Accepts text from the user.
5.  Converts the text into a sequence.
6.  Pads the sequence.
7.  Runs the LSTM model.
8.  Returns the predicted next word.

## ⚙️ Installation

### 1. Clone the repository

``` bash
git clone https://github.com/tirthkoradia45/Next_word_prediction.git
cd Next_word_prediction
```

### 2. Create a virtual environment

``` bash
python -m venv .venv
```

Activate it on Windows:

``` bash
.venv\Scripts\activate
```

On macOS/Linux:

``` bash
source .venv/bin/activate
```

### 3. Install dependencies

Install the required packages:

``` bash
pip install streamlit tensorflow numpy
```

## ▶️ Run the Application

Start the Streamlit application with:

``` bash
streamlit run app.py
```

The application will open in your browser.

Enter a sentence in the text box and click:

**Predict Next Word**

## 📊 Model Components

### LSTM Model

LSTM is a type of Recurrent Neural Network (RNN) designed to learn
dependencies in sequential data.

For text prediction, the model learns relationships between words based
on the sequences present in the training data.

### Tokenizer

`tokenizer.pkl` stores the tokenizer used during model training. It
ensures that user input is converted into the same numerical
representation expected by the trained model.

### Maximum Sequence Length

`max_len.pkl` stores the sequence-length configuration used during
training and inference.

### Trained Model

`lstm_model (1).h5` contains the trained LSTM model used by the
Streamlit application.

## 📓 Notebooks

### `RNNimplementation.ipynb`

Contains the main implementation and experimentation related to the
recurrent neural network / LSTM approach.

### `codefile.ipynb`

Contains supporting code and experimentation used during development.

## 📈 Dataset

The project uses `qoute_dataset.csv` as the text dataset.

The text data is used to create sequences that allow the model to learn
relationships between words and predict the next word.

## 🎯 Use Cases

Next-word prediction can be used as a foundation for:

-   Smart text completion
-   Search suggestions
-   Writing assistants
-   Keyboard prediction
-   Chat interfaces
-   NLP-based autocomplete systems

## 🔮 Future Improvements

Some possible improvements include:

-   Predict the top 3--5 most likely next words instead of only one
-   Improve text preprocessing and cleaning
-   Use a larger and more diverse dataset
-   Add temperature-based sampling for more varied predictions
-   Compare LSTM with GRU and Transformer-based models
-   Improve the Streamlit UI
-   Add model evaluation metrics
-   Deploy the application publicly
-   Add multi-word text generation

## 📌 Learning Outcomes

Through this project, I worked with:

-   Natural Language Processing
-   Text tokenization
-   Sequence generation
-   Padding sequences
-   Recurrent Neural Networks
-   LSTM networks
-   TensorFlow/Keras
-   Model serialization
-   Streamlit application development
-   Deploying a trained deep learning model for inference

## 👨‍💻 Author

**Tirth Patel**

GitHub: [@tirthkoradia45](https://github.com/tirthkoradia45)

## 📜 License

This project is intended for educational and portfolio purposes.
