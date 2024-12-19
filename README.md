# Document and Code Plagiarism Detector

## Overview
The Document and Code Plagiarism Detector is a Streamlit-based application that allows users to:

- Compare documents for text and code plagiarism.
- Generate similarity reports for documents and code snippets.
- Detect and analyze similarities in content and code with support for multiple file formats.

This tool utilizes state-of-the-art technologies such as BERT for text similarity and Gemini API for code translation, ensuring accurate and efficient plagiarism detection.

## Features
- **Document Comparison**:
  - Supports `.txt`, `.pdf`, `.docx`, and `.csv` formats.
  - Extracts and analyzes both textual content and embedded code snippets.
- **Code Similarity Analysis**:
  - Supports `.c`, `.cpp`, `.py`, and `.js` code files.
  - Converts code snippets into a common language for comparison (e.g., C++).
  - Computes similarity scores for code snippets with normalized comparisons.
- **Detailed Reports**:
  - Generates and downloads plagiarism reports in markdown format.
- **Easy-to-Use Interface**:
  - Intuitive Streamlit UI for uploading files and viewing results.
  - Sidebar instructions and supported file formats for user guidance.

## Technologies Used
- **Streamlit**: For building the user interface.
- **PyPDF2**: For processing PDF documents.
- **docx**: For extracting text from Word documents.
- **Pandas**: For handling CSV data.
- **Transformers** (Hugging Face): For BERT-based text similarity analysis.
- **Google Generative AI**: For code conversion between programming languages.
- **Torch**: For computing text similarity using BERT embeddings.
- **difflib**: For detecting and comparing matching sections of text and code.

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- pip package manager

### Steps
1. Clone this repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd <repository-directory>
   ```
3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up the Gemini API key:
   - Replace the placeholder API key in the `genai.configure` method with your own API key.
   - Obtain an API key from Google Generative AI services if you don’t have one.

5. Run the application:
   ```bash
   streamlit run model.py
   ```

## Usage
1. Open the application in your web browser (default URL: `http://localhost:8501`).
2. Follow these steps:
   - Upload two documents for text similarity analysis.
   - Optionally, upload two code files for plagiarism detection.
   - Wait for the analysis to complete.
3. View the results:
   - Similarity metrics will be displayed on the screen.
   - Download detailed reports for documents and code comparisons.

## Supported Formats
### Document Formats
- `.txt`
- `.pdf`
- `.docx`
- `.csv`

### Code Formats
- `.c`
- `.cpp`
- `.py`
- `.js`

## Key Functionalities
- **Extract Text**: Extracts text and code snippets from supported file types.
- **Text Analysis**: Computes similarity using BERT embeddings and finds matching sections.
- **Code Conversion**: Converts code snippets to C++ (if not already in C++) for unified comparison.
- **Similarity Calculation**: Computes overall similarity scores for both documents and code snippets.
- **Report Generation**: Creates downloadable markdown reports summarizing the findings.

## File Structure
```
.
├── model.py                  # Main application script
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation

```

## Known Issues
- Processing large files may take time.
- Requires a valid Gemini API key for code conversion.

## Future Enhancements
- Add support for additional file formats (e.g., `.html`, `.xml`).
- Improve speed and performance for large documents.
- Introduce advanced visualizations for similarity results.

## License
This project is licensed under the MIT License.

## Acknowledgements
- [Streamlit](https://streamlit.io/)
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Google Generative AI](https://developers.google.com/)

## Contact
For questions or suggestions, feel free to contact Prashant kumar jha at jhakumarprasant111@gmail.com.

