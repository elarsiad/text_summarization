# Text Summarization with BERT-based Encoder-Decoder

This project trains a BERT-based encoder-decoder model to generate abstractive summaries of Indonesian news articles from Liputan 6. 

## Description

The model is implemented using HuggingFace EncoderDecoderModel and fine-tuned on a dataset of Indonesian news articles and human-written summaries. It uses a BERT encoder and a separate BERT decoder with tied embeddings. The data is split into training, validation, and test sets.

The data preprocessing includes tokenization using a TinyBERT tokenizer and adding special tokens.

Evaluation uses ROUGE scores between model-generated and human summaries on a held-out test set.

## Files

The code loads and preprocesses the DataFrames:

- c_train_df_5k.csv: 5,000 training article-summary pairs  
- c_dev_df.csv: validation set
- c_test_df.csv: test set

The main model training loop is in the notebook file.

## Future Work

Potential improvements:

- Train for more epochs to improve summarization quality
- Experiment with different model architectures and sizes 
- Include document context by using longformer self-attention
- Improve handling of Indonesian language syntax and grammar