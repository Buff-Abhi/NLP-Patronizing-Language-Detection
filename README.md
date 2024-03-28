# NLP-Patronizing-Language-Detection
Patronizing and Condescending Language Detection using Natural Language Processing Models

# Project Summary
The project focused on the SemEval-2022 Task 4 - Patronizing and Condescending Language Detection, a binary classification task. The goal was to develop a system that can detect the presence of patronizing and condescending language (PCL) in paragraphs extracted from news articles in English.

# Data
The dataset used for this task is the Don't Patronize Me! dataset, which contains 10,636 paragraphs annotated for the presence of PCL. Each paragraph is labeled on a scale from 0 (not containing PCL) to 4 (highly patronizing or condescending) towards vulnerable communities. The dataset is provided in the dontpatronizeme_pcl.tsv file, where each line contains the paragraph ID, keyword, country code, paragraph text, and the corresponding label.

# Approach
* Data Exploration: The team began by analyzing the training dataset and observed that it was skewed, with significantly more data for non-PCL paragraphs than for PCL paragraphs.
* Model Selection: After reviewing relevant research papers, the team decided to use a Bidirectional Long Short-Term Memory (BiLSTM) model for the binary classification task. This decision was based on the team's familiarity with TensorFlow and BERT resources.
* Data Preprocessing: The team used the BERT tokenizer to create word embeddings for the paragraphs. The tokenized data was then padded to ensure uniform input lengths for the LSTM model.
* Model Architecture: The model was built using a sequential architecture, consisting of an embedding layer, three BiLSTM layers, and an output layer with a sigmoid activation function.
* Hyperparameter Tuning: The team experimented with various hyperparameters, such as batch size, embedding output dimensions, loss function, epochs, and optimizer. The final configuration included a batch size of 512, embedding output dimensions of 10, binary cross-entropy loss, 20 epochs, and the Adam optimizer.
* Performance Monitoring: The team tracked the model's performance using a graph that displayed training accuracy, testing accuracy, training loss, and testing loss over the epochs. The results varied due to the shuffling of the training data, with the highest F1 score reaching around 0.44 and an average F1 score of 0.35.
