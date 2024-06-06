# Product Information Retrieval with Gemini and LangChain

This project demonstrates a hybrid approach for retrieving product information using both text and image queries. It leverages Google's Gemini generative AI models for text and vision processing and uses `DocArrayInMemorySearch` from the LangChain library for efficient in-memory similarity searches.

## Table of Contents

- [Project Overview](#project-overview)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [License](#license)

## Project Overview

This project includes the following steps:
1. Loading and processing text data.
2. Generating text chunks and embeddings.
3. Handling text queries.
4. Handling image queries.
5. Performing similarity searches with image descriptions.
6. Combining results from text and image queries.
7. Generating a comprehensive response using the Gemini models.

## Setup Instructions

### Prerequisites

- GitHub account
- OpenAI API key (for Gemini models)

### Steps

1. **Clone the repository**:

    ```bash
    git clone https://github.com/imranajec/gemini-langchain-product-info-retrieval.git
    cd gemini-langchain-product-info-retrieval
    ```

2. **Install Dependencies**:

    ```bash
    pip install transformers langchain faiss-cpu requests pillow matplotlib
    ```

3. **Prepare Your Data**:
   - Ensure you have your text data file (e.g., `product_catalog.txt`) and image file (e.g., `35861_01.jpg`) in the appropriate directory.

4. **Set the OpenAI API key**:

    Ensure you have your OpenAI API key available in your environment:

    ```python
    import os
    os.environ["OPENAI_API_KEY"] = "your_openai_api_key"
    ```

5. **Run the Jupyter Notebook**:

    Open `gemini-langchain-product-info-retrieval.ipynb` in Jupyter Notebook and run the cells sequentially.

## Usage

1. **Load and Process Text Data**:
    - The notebook will load the specified text file and split it into chunks.

2. **Generate Text Chunks and Embeddings**:
    - The text chunks are used to generate embeddings and stored in a vector store using `DocArrayInMemorySearch`.

3. **Handle Text Query**:
    - Perform a similarity search using a text query to retrieve relevant documents.

4. **Handle Image Query**:
    - Process a local image file and analyze it with the Gemini vision model to generate a textual description.

5. **Perform Similarity Search with Image Description**:
    - Perform a similarity search using the text generated from the image description to retrieve relevant documents.

6. **Combine Results**:
    - Combine the results from the text query and image analysis.

7. **Generate a Response**:
    - Generate and display a comprehensive response based on the combined context using the Gemini models.

## Dependencies

The following Python libraries are required:

```plaintext
transformers
langchain
faiss-cpu
requests
pillow
matplotlib
