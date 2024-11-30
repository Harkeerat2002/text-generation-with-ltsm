# Project Title: Generation of News Titles using LSTM
**Student: Harkeerat Singh Sawhney**
# Overview
This project aims to generate news titles using a Long Short-Term Memory (LSTM) model. The dataset used for this project is the News Category Dataset from Kaggle. The project involves data preprocessing, model training, and generating news titles using different sampling strategies.

# Directory Structure
```bash
data/
    all_words.pkl
    int_to_word.pkl
    tokenized_title.pkl
    word_to_int.pkl
harkeerat_sawhney.py
plots/
README.md
report/
    harkeerat_sawhney.aux
    harkeerat_sawhney.log
    harkeerat_sawhney.out
    harkeerat_sawhney.tex
    plots/
```
# Files
- `harkeerat_sawhney.py`: Main Python script containing the implementation of the LSTM model, data preprocessing, training and generation of news titles.
- `data/`: Directory containing preprocessed data files.
- `plots/`: Directory for storing plots (if any).
- `report/`: Directory containing the LaTeX report and related file
# Main Components
## Data Preprocessing
1. Download Data: The dataset is downloaded and filtered to include only the "POLITICS" category.
2. Tokenization: Headlines are tokenized and saved.
3. Dictionaries: word_to_int and int_to_word dictionaries are created for converting words to integers and vice versa.
4. Dataset Class: A custom TextDataset class is implemented to handle the dataset.
## Model Implementation
- LSTMModel: An LSTM model is implemented with embedding, LSTM, dropout, and fully connected layers.
- Initialization: The model is initialized with parameters such as vocabulary size, embedding dimension, hidden dimension, number of layers, and dropout probability.
## Training
- Training Loop: The model is trained using a standard training loop with cross-entropy loss and Adam optimizer.
- Train with TBBTT: Training with Truncated Backpropagation Through Time (TBBTT) is implemented for better performance.
## Generation of News Titles
- Sampling Strategies: Two sampling strategies are implemented:
random_sampler_next: Samples the next word based on probabilities.
sampler_argmax: Samples the next word with the highest probability.
- Sample Function: Generates news titles using the trained model and the specified sampling strategy.
# Achievements
- Successfully implemented an LSTM model for generating news titles.
- Preprocessed the dataset and created necessary dictionaries for tokenization.
- Trained the model using both standard training and TBBTT.
- Generated news titles using different sampling strategies.
- Documented the process and results in a LaTeX report.