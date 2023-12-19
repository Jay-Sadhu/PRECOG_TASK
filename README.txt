# Word Embedding and Clustering with GloVe and KMeans

## Overview

This repository contains a Python script for generating word embeddings using GloVe pre-trained word vectors and performing clustering on a text dataset using KMeans. The main goal is to organize words into clusters based on their semantic similarity.

## Directory Structure

- /content/drive/MyDrive/Colab Notebooks/: The main directory containing the script and necessary data files.
- /content/drive/MyDrive/Colab Notebooks/glove.6B.100d.txt: GloVe pre-trained word vectors file.
- /content/drive/MyDrive/Colab Notebooks/SimLex-999.txt: SimLex999 dataset for evaluating the clustering results.
- /content/drive/MyDrive/Colab Notebooks/brown.csv: Brown Corpus data for training word embeddings.
- /content/drive/MyDrive/Colab Notebooks/Token.csv: Dataset containing preprocessed text of Brown Corpus.

## Dependencies

Ensure the following Python libraries are installed before running the script:
- pandas
- scikit-learn
- gensim
- numpy
- nltk


Approach
1. Data Loading and Preprocessing:
- SimLex999 and Brown Corpus data are loaded into Pandas DataFrames.
- Text preprocessing is applied to tokenize and remove stop words from the Brown Corpus data.

2.Word Embeddings with GloVe:
- GloVe word vectors are loaded and used to create word embeddings for each tokenized sentence in the Brown Corpus.

3.Clustering with KMeans:
- Cosine similarity is calculated between word embeddings in chunks.
- KMeans clustering is performed on the cosine similarity matrix in chunks to handle memory constraints.

4.Evaluation with SimLex999:
- The script evaluates the clustering results using SimLex999 dataset, calculating average similarity within clusters.

5. Spearman Correlation:
- The script calculates Spearman correlation between the predicted similarities from clustering and the actual similarities from SimLex999.











# Word Embedding with GloVe and exploring Cosine Simmilarity in detail

I have thought of doing this implementation and could not due computational restritions. On 19-12-2023(i.e last day of submission) I got access to DGX. So I thought including this code as well. Please go through it as well.

  

This repository contains a Python script for generating word embeddings using GloVe pre-trained word vectors, mapping word similarities, and evaluating the results using the SimLex999 dataset.

## Directory Structure

- /dgxa_home/se20uari151/: The main directory containing the script and necessary data files.
- /dgxa_home/se20uari151/glove.6B.100d.txt : GloVe pre-trained word vectors file.
- /dgxa_home/se20uari151/SimLex-999.txt : SimLex999 dataset for evaluating word similarities.
- /dgxa_home/se20uari151/brown.csv: Brown Corpus data for training word embeddings.
- /dgxa_home/se20uari151/token.csv: Dataset containing preprocessed text of Brown Corpus.



Certainly! Here's a README template for your codebase:

markdown
Copy code
# Word Embedding and Similarity Mapping with GloVe

## Overview

This repository contains a Python script for generating word embeddings using GloVe pre-trained word vectors, mapping word similarities, and evaluating the results using the SimLex999 dataset.

## Directory Structure

- /dgxa_home/se20uari151/: The main directory containing the script and necessary data files.
  - /dgxa_home/se20uari151/glove.6B.100d.txt: GloVe pre-trained word vectors file.
  - /dgxa_home/se20uari151/SimLex-999.txt: SimLex999 dataset for evaluating word similarities.
  - /dgxa_home/se20uari151/brown.csv: Brown Corpus data for training word embeddings.
  - /dgxa_home/se20uari151/token.csv: Dataset containing preprocessed text.

## Dependencies

Ensure the following Python libraries are installed before running the script:

- pandas
- scikit-learn
- gensim
- numpy
- nltk


Approach
1.Data Loading and Preprocessing:
- SimLex999 and Brown Corpus data are loaded into Pandas DataFrames.
- Text preprocessing is applied to tokenize and remove stop words from the Brown Corpus data.

2.Word Embeddings with GloVe:
- GloVe word vectors are loaded and used to create word embeddings for each tokenized sentence in the Brown Corpus.

3.Mapping Similarity:
- Cosine similarity is calculated between word embeddings for a subset of the data.
- A linear transformation is applied to map similarity values from [-1, 1] to [0, 10].

4.Evaluation with SimLex999:
- The script evaluates the mapping results using the SimLex999 dataset.
- The Spearman correlation coefficient is calculated between actual and mapped similarity values.


