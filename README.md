Problem Statement
Clinical notes are rich in unstructured data, containing information about a patient’s condition, symptoms, and treatment. The goal of this project is to automatically extract medical entities from clinical text using NER, and to evaluate the semantic similarity between clinical case descriptions to identify related diagnoses.
To accomplish this, I will implement and compare two types of models for the NER task: a Conditional Random Field (CRF)-based tagger and a transformer-based BERT model. In the second part of the project, I will use Word2Vec and BERT embeddings to calculate paragraph-level similarity between clinical descriptions and cluster them to assess potential diagnostic groupings. This combined pipeline could be used to support diagnosis prediction or flagging of similar historical patient cases in real-world clinical data systems.
Actual use cases inspire this project in clinical data science, and each component builds on concepts explored in prior class assignments — including BERT-based paragraph similarity (Assignment 1), semantic embedding relationships (Assignment 2), and NER using CRF and BERT (Assignment 3).

Dataset: Synthetic Clinical NER Dataset
After much trouble getting publicly available or synthetic clinical notes that include mentions of symptoms, diagnoses, and medical conditions, I decided to generate a synthetic dataset of 75 anonymized clinical snippets for proof-of-concept purposes, manually tagging them to identify named entities, including diseases, symptoms, drugs, and tests. These will be structured similarly to the CoNLL-2003 format for CRF and token classification tasks.
The data will be preprocessed with standard NLP techniques including lowercasing, tokenization, and entity labeling.

Expected Results
I expect the BERT-based model to outperform the CRF model in NER tasks, particularly with more complex or ambiguous entities. For semantic similarity, BERT embeddings should yield more context-aware similarity scores than Word2Vec, especially when comparing longer clinical paragraphs. Clustering on paragraph embeddings is anticipated to group similar clinical cases (e.g., respiratory vs. cardiovascular cases), showing promise for diagnosis recommendation systems.

Key metrics will include:
For NER: Precision, Recall, F1-Score.
For Similarity: Cosine similarity scores and qualitative cluster evaluations.
