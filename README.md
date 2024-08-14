# RM_ASSIGNMNT3_LLM
Research module assignment-3

INTRODUCTION:
	One of the core tasks in NLP is sentiment analysis, which can be explained as determining the sentiment expressed in a piece of text. We explain the process and results for fine-tuning two pre-trained large language models, BERT and RoBERTa, on an Amazon dataset shoe review. The main task was the classification of reviews provided by customers into sentiment categories ranging from "Very poor" to "Excellent."
Dataset selection: For our work, we opted to use the Amazon Shoe Ratings dataset from based on its diversity of nature, size, and relevance. The collection has thousands of customer reviews with a wide range of sentiment expressions. Each is attached to an emotion label at a scale from 0 to 4, where 0 is "Very poor," and 4 is "Excellent.". The huge number of real-world textual content that lies in this dataset makes for a challenging context of testing and optimizing pre-trained LLMs. It further enables training models directly relevant to e-commerce platforms where business intelligence is key and depends upon the analysis of users' sentiments.

Dataset and Exploratory Data Analysis (EDA):
	Before fine-tuning the models, an Exploratory Data Analysis was done to understand some characteristics of the dataset. This included checking the distribution of labels and their sentiment labels and the length of the reviews.
•	Label Distribution: The dataset is well balanced in terms of distribution of labels. As such, we were assured that our model would not be biased to any class of sentiment while training.
•	Length of Review: The lengths of the reviews varied to a great extent, requiring proper care during tokenization to deal with the variation and extract meaningful input sequences.
These insights guided the selection of parameters to the model, such as the maximum sequence length for tokenization and the need for handling class imbalances.

METHODOLOGY:
	The methodology for fine-tuning the BERT and RoBERTa models involved several key steps:
1.	 Data Pre-processing:
•	Tokenization: The text data was tokenized into the respective tokens with the respective tokenizers for BERT and RoBERTa. In tokenization, the textual data gets converted into numerical form. It involves breaking down the text into tokens and then making a mapping to the corresponding IDs for the tokens. This step consists of padding the shorter sequences and trimming the longer ones to uniform input data of equal length, but not more than a maximum sequence length.
•	Data Split: The dataset shall be divided into three parts: one with a share of 70% for training, another 15% for validation, and the remaining 15% for testing. The training set will be used to fine-tune the model, the validation set for hyperparameter tuning, and the test set for the final performance evaluation.
2.	Model Training and fine tuning:
•	Model Initialization: Pre-trained BERT and RoBERTa models were loaded with their pre-trained weights.
o	Optimization: We used the Adam optimizer with different learning rates for each model to ensure convergence. We had tried earlier for the choice of learning rates.
o	Regularization: Dropouts were tuned to avoid overfitting, and early stopping was performed on validation loss.
o	The metrics that tracked model performance on the training data included accuracy and loss.

RESULTS:
	The performance of both models on the test dataset was compared based on accuracy and loss:
BERT Model:           	         RoBERTa Model:
Test accuracy: 60.0%	           Test accuracy: 66.0%
Test loss: 1.064	               Test loss: 0.875
•	Both models achieved satisfactory accuracy, but RoBERTa outperformed BERT with a higher accuracy and lower test loss.
•	The lower loss for RoBERTa indicates that its predictions were not only more accurate but also more confident and better calibrated. 

CONCLUSION: 
In summary, RoBERTa fared better than BERT for this sentiment analysis assignment on Amazon shoe reviews in terms of prediction accuracy and confidence. This study illustrated the advantages of utilizing more sophisticated models like RoBERTa over more basic ones like BERT and showed how successful it is to fine-tune pre-trained language models on tasks.
