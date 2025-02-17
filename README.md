# Multi-Model RAG System

## Overview
This project implements a **multi-model Retrieval-Augmented Generation (RAG) system** that combines **deep learning-based text classification**, **semantic search with FAISS**, and **transformer-based embeddings** to retrieve and classify textual data efficiently.

## Features
- **Text Preprocessing**: Cleans and normalizes input text data.
- **BERT-based Transformers**: Uses `BERT` and `AutoModelForSequenceClassification` for encoding text into meaningful embeddings.
- **FAISS Vector Search**: Utilizes FAISS for efficient similarity-based retrieval of relevant documents.
- **Custom PyTorch Dataset**: Implements a dataset class to handle text-label mappings.
- **Multi-Model Approach**: Combines different transformers for text understanding and retrieval.

## Installation
Before running the project, install the required dependencies:
```bash
pip install torch transformers faiss-cpu pandas numpy
```

## Usage
1. **Prepare the Dataset**
   - Ensure that the dataset (CSV file) is in the correct format.
   - The text column should be defined for processing.

2. **Run the Model**
   - Modify the `df` variable to load your dataset.
   - Define the text column (`text_column`).
   - Execute the script to train and evaluate the model.

3. **Retrieval and Classification**
   - Input a query.
   - The system will retrieve similar documents using FAISS and classify them using transformers.

## Dataset
- The dataset should be a CSV file containing textual data in a specified column.
- Labels are mapped using a predefined dictionary.
- Example columns: `Complaint/Opinion`, `Category`, `Entity`.

## How It Works
1. **Text Preprocessing**: Converts text to lowercase and removes unnecessary characters.
2. **Embedding Generation**: Uses BERT-based models to generate text embeddings.
3. **Vector Indexing with FAISS**: Stores embeddings for efficient similarity search.
4. **Classification**: Maps retrieved text to pre-defined categories.

## Future Improvements
- Support for **multi-lingual** models.
- Integration with **LlamaIndex** for enhanced document retrieval.
- Optimization for **real-time** performance.

## Contributors
Amaan Ali
Ms. Sarmistha Das

For any questions, feel free to raise an issue!

