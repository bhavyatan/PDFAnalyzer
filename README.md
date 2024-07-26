

---

# PDFAnalyzer

PDFAnalyzer is a Streamlit application that allows users to analyze and interact with PDF documents using Google's Generative AI and LangChain. By uploading PDF files, users can extract and query information through an AI-powered chatbot interface. The application leverages FAISS for vector storage and retrieval to provide fast and accurate answers from PDF content.

## Features

- **Upload PDF Files**: Users can upload one or multiple PDF documents for analysis.
- **Text Extraction**: Automatically extracts text from uploaded PDFs using PyPDF2.
- **Chunking**: Splits extracted text into manageable chunks for better processing.
- **AI-Powered Q&A**: Utilizes Google Generative AI and LangChain to answer questions based on the document content.
- **Vector Storage**: Stores document embeddings in a FAISS vector store for efficient retrieval.

## Installation

To get started with PDFAnalyzer, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/pdfanalyzer.git
    cd pdfanalyzer
    ```

2. **Set up a virtual environment**:
    ```bash
    python -m venv env
    source env/bin/activate  # On Windows use `env\Scripts\activate`
    ```

3. **Install the required packages**:
    ```
    pip install -r requirements.txt
    ```

4. **Set up environment variables**:
    - Create a `.env` file in the root directory.
    - Add your Google API key to the `.env` file:
      ```
      GOOGLE_API_KEY=your_google_api_key_here
      ```

## Usage

To run the application, execute the following command:

```
streamlit run pdf_analyzer.py
```

Once the server is running, open your browser and go to `http://localhost:8501` to interact with PDFAnalyzer.

### Analyzing PDFs

1. **Upload PDFs**: Use the sidebar to upload one or multiple PDF documents.
2. **Analyze**: Click the "Analyze" button to extract text and create embeddings.
3. **Ask Questions**: Enter your questions in the text input box and get responses based on the PDF content.

## How It Works

### Text Extraction

The application uses `PyPDF2` to extract text from uploaded PDF files. Extracted text is then split into chunks using `RecursiveCharacterTextSplitter` for efficient processing.

### AI-Powered Question Answering

PDFAnalyzer leverages Google's Generative AI model for embeddings and LangChain for constructing conversational chains. The AI model processes user questions against the stored document chunks to generate accurate responses.

### Vector Store

Document embeddings are stored in a FAISS vector store, allowing for fast similarity search and retrieval. This ensures that questions are answered based on relevant document sections.

## File Structure

- **pdf_analyzer.py**: Main application script.
- **requirements.txt**: List of required Python packages.
- **.env**: Environment variables file (not included in the repository).

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License.

## Acknowledgments

- [Streamlit](https://streamlit.io/)
- [LangChain](https://github.com/hwchase17/langchain)
- [PyPDF2](https://github.com/py-pdf/pypdf)

---

