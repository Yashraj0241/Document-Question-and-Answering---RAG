# Data Science Document Q&A

This project is a **Document Question-Answering** application powered by the **Gemma Model** and **Streamlit**. It allows users to upload documents, create a vector store for document embedding, and ask questions directly related to the uploaded content. The answers are generated based on the context from the documents.

---

## Features

- **Interactive UI**: Built with Streamlit for easy interaction.
- **PDF Document Processing**: Load and process documents stored in the `./data` directory.
- **Vector Store Creation**: Generate vector embeddings for documents using **FAISS** and **Google Generative AI Embeddings**.
- **Advanced Question Answering**: Use the **Gemma Model (gemma2-9b-it)** to generate accurate, context-specific answers.
- **Document Similarity Search**: Display relevant document chunks used to generate the answer.
- **Real-Time Response Time**: Measure and display the time taken to generate a response.
- **Multi-Document Support**: Handles multiple documents seamlessly for broader context.
- **Content Summary Feature**: Generate summaries of document content to provide quick insights.

---

## Tech Stack

- **Python**
- **Streamlit**
- **FAISS** (Facebook AI Similarity Search)
- **Google Generative AI** for embeddings
- **LangChain** for processing and chains
- **dotenv** for secure environment variable handling

---

## Installation and Setup

### Prerequisites

- Python 3.8 or higher
- `pip` (Python package installer)

### Steps to Run

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Set Up a Virtual Environment**
   ```bash
   python -m venv llm_env
   source llm_env/bin/activate   # On Windows: llm_env\Scripts\activate
   ```

3. **Install Required Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Prepare Environment Variables**
   - Create a `.env` file in the project root directory.
   - Add the following keys:
     ```
     GROQ_API_KEY=<your_groq_api_key>
     GOOGLE_API_KEY=<your_google_api_key>
     ```

5. **Prepare Data**
   - Place your PDF files inside the `./data` directory.

6. **Run the Application**
   ```bash
   streamlit run app.py
   ```

7. **Access the App**
   - Open your browser and go to [http://localhost:8501](http://localhost:8501).

---

## Usage

1. **Initialize Vector Store**:
   - Click the **"Create Vector Store"** button to prepare the vector database.

2. **Ask Questions**:
   - Type your question in the input field, e.g., "What is the purpose of this document?"
   - Press Enter to get an answer.

3. **View Similar Documents**:
   - Expand the **"Document Similarity Search"** section to view relevant document chunks used to generate the answer.

4. **Generate Content Summaries**:
   - Use the new summary feature to generate concise summaries of the uploaded documents.

5. **Response Time**:
   - Monitor real-time response time displayed below the answer for performance insights.

---

## File Structure

```
|-- data/                     # Directory for storing PDF documents
|-- app.py                    # Main Streamlit application code
|-- requirements.txt          # Required dependencies
|-- .env                      # Environment variables (not included in the repo)
|-- README.md                 # Project documentation
```

---

## Troubleshooting

- **Vector Store Not Ready:**
  - Ensure you click the "Create Vector Store" button before asking questions.
- **API Key Errors:**
  - Verify that your `.env` file contains valid API keys.
- **Dependencies Issues:**
  - Run `pip install -r requirements.txt` to ensure all required packages are installed.
- **No Response Generated:**
  - Check if the uploaded documents are correctly processed.
  - Verify the document format and ensure the data folder is not empty.

---

## Future Enhancements

- Add support for more document formats (e.g., `.txt`, `.docx`, `.csv`).
- Include progress indicators for vector store creation.
- Implement keyword-based document filtering.
- Enable multi-user sessions in Streamlit.
- Add a feature to visualize embeddings for enhanced debugging and analysis.
- Introduce caching for frequently asked questions to improve response time.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Author

- **Your Name**  
  [GitHub Profile](https://github.com/your-profile) | [LinkedIn](https://www.linkedin.com/in/your-profile)

---

Feel free to fork, contribute, or open issues for improvements! 🎉
