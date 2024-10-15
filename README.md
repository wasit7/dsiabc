# dsiabc

Assessment Instructions for DSI441 Deep Learning Class

Objective: The objective of this assessment is to train sequence-to-sequence models (RNN, LSTM, and Transformer) on music data represented in 12-key * 8-octave tokenization, using ABC notation as input.


---

1. Prepare Data

1.1. Input ABC Notation

Obtain a dataset in ABC music notation format. Use the following suggested sources:

ABC Notation Archive

Session.org

Mutopia Project


Choose a small subset of music data that contains simple melodic lines. The dataset should include various music pieces spanning different octaves.


1.2. Convert to 12-key * 8-octave Tokenization

Implement a Python function that converts ABC notation into a 12-key (12 semitones) representation, spanning 8 octaves.

Each note in the ABC format should be converted to a token based on the note (A-G), its accidentals (sharps/flats), and the octave (e.g., C4, A#5).

Use the provided mapping from the ABC notation to 12-key tokenization (12k notation), where each note is mapped to a unique integer value. Ensure the conversion spans 8 octaves, providing a total of 96 unique tokens (12 semitones * 8 octaves).



---

2. Train Sequence-to-Sequence Models

Implement and train the following models for predicting music sequences from the tokenized ABC notation data:

2.1. RNN Model

Create a Recurrent Neural Network (RNN) model using PyTorch or TensorFlow.

Train the RNN on the tokenized sequences to predict the next token in a sequence.


2.2. LSTM Model

Implement an LSTM model to learn the patterns in the tokenized music sequences.

Ensure the model can handle long-term dependencies in the music.


2.3. Transformer Model

Implement a minimal transformer model with an encoder and decoder architecture.

Use positional encoding to enhance the sequence representation.


For each model:

Use the tokenized input sequences as training data.

Set appropriate hyperparameters for learning (batch size, learning rate, etc.).

Train the models for a fixed number of epochs (e.g., 100 epochs).



---

3. Evaluation

For each model, perform the following evaluations:

3.1. Prediction Accuracy

After training, use the trained model to generate music sequences.

Compare the predicted sequences to the actual target sequences using metrics such as cross-entropy loss or mean squared error.


3.2. Model Performance

Record the training and validation loss over the epochs.

Evaluate the models on a held-out test set and report the accuracy.


3.3. Musical Coherence

Evaluate the generated music sequences for their musical coherence (e.g., do the sequences sound like valid melodies?).

You may generate MIDI files from the predicted sequences for manual listening evaluation.



---

Deliverables:

Code for data preparation and model training.

Training logs showing loss and accuracy over time.

Generated music sequences from each model.

A brief report comparing the performance of RNN, LSTM, and Transformer models, including both quantitative metrics and qualitative observations on the generated music.


Submission Deadline: 2 weeks
