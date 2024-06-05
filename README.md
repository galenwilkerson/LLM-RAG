# LLM-RAG - There are things an LLM doesn't know and must look up.

A simple example of retrieval augmented generation (RAG) for LLMs.

This repository provides a simple implementation of a Retrieval-Augmented Generation (RAG) system using smaller pre-trained models from the Hugging Face Transformers library. The implementation is demonstrated in a Jupyter Notebook named `LLM RAG example.ipynb`.

## Overview

**Retrieval-Augmented Generation (RAG)** is a technique that enhances the generation capabilities of language models by incorporating external knowledge through retrieval. It combines two main components:
1. **Retriever**: Finds relevant documents from a predefined knowledge base based on the input query.
2. **Generator**: Uses both the input query and the retrieved documents to generate a more accurate and informative response.

## Implementation Details

This implementation uses:
- **DistilBERT**: A smaller, faster version of BERT for the retriever component.
- **T5-small**: A smaller version of T5 for the generator component.

The script follows these steps:
1. **Install necessary packages**: Installs `transformers`, `datasets`, and `sentencepiece`.
2. **Load pre-trained models and tokenizers**: Loads `DistilBERT` for retrieval and `T5-small` for generation.
3. **Create a knowledge base**: A simple list of documents.
4. **Retrieve relevant documents**: Encodes the query and documents, computes similarity scores, and retrieves the top-k documents.
5. **Generate a response**: Uses the retrieved documents as context to generate a response to the input query.

## Prerequisites

- Python 3.6 or higher
- Jupyter Notebook

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/LLM-RAG.git
    cd LLM-RAG
    ```

2. Install the required packages:
    ```sh
    pip install transformers datasets sentencepiece
    ```

## Usage

1. Open the Jupyter Notebook:
    ```sh
    jupyter notebook LLM\ RAG\ example.ipynb
    ```

2. Follow the instructions in the notebook to run the RAG system example. The notebook includes sections to:
    - Load pre-trained models and tokenizers.
    - Create a simple knowledge base.
    - Retrieve relevant documents based on an input query.
    - Generate a response using the retrieved documents.

## Example

An example query and response using the system:
```sh
Query: What color is the sky?
Response: The sky is blue.
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an issue.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Hugging Face for providing the `transformers` library.
- The developers of `datasets` and `sentencepiece`.

