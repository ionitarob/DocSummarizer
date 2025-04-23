# DocSummarizer-Student

**DocSummarizer-Student** is an offline, open-source tool tailored for students who need to extract and organize study notes from lengthy documents (PDF, DOCX, TXT) and automatically generate presentations (PPTX) or enriched Word documents (DOCX) from those notes.

---

## Key Features

1. **Executive Summary**: Produce a concise, high-level summary of any long document.
2. **Structured Notes**: Extract headings, subheadings, and key points, formatting them into well-organized study notes.
3. **PowerPoint Export**: Automatically generate slides for each key section.
4. **DOCX Export**: Create a Word document containing the summary and structured notes.
5. **Offline & Free**: Runs entirely on CPU without internet access, using only open-source libraries.

---

## Tech Stack

- **Text Extraction**: `pdfplumber` / `PyMuPDF` (PDF), `python-docx` (DOCX), plain text.
- **Preprocessing**: Text cleaning and segmentation with **NLTK** or **spaCy**.
- **Summarization**: Hugging Face Transformers (e.g., T5-small or quantized PEGASUS).
- **PPTX Generation**: `python-pptx`.
- **DOCX Generation**: `python-docx`.
- **Interface**: **Streamlit** or **Gradio** for an optional web demo.
- **Environment Management**: `requirements.txt` or `environment.yml`, optional Dockerfile.

---

## Installation

```bash
git clone https://github.com/your-username/DocSummarizer-Student.git
cd DocSummarizer-Student
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## Basic Usage

1. Place your document(s) in the `input/` directory.
2. Run the CLI or launch the web interface:
   ```bash
   # CLI
   docsum --input input/my_document.pdf --mode notes --output output/

   # Web interface
   streamlit run app.py
   ```
3. Check the `output/` folder for:
   - `my_document_summary.txt`
   - `my_document_notes.docx`
   - `my_document_slides.pptx`

---

## Project Structure

```
DocSummarizer-Student/
├── input/                # Input documents
├── output/               # Generated files
├── docs/                 # Additional documentation and examples
├── src/
│   ├── extract/          # Text extraction modules
│   ├── preprocess/       # Cleaning and segmentation
│   ├── summarizer/       # Summarization model wrappers
│   ├── exporters/        # PPTX and DOCX generators
│   └── cli.py            # Command-line interface
├── app.py                # Streamlit/Gradio web interface
├── requirements.txt
└── README.md
```

---

## Next Steps / MVP

1. **Extraction Module**: Implement PDF and DOCX readers.
2. **Basic Summarizer**: Integrate T5-small to generate simple summaries.
3. **Minimal CLI**: Process a document and output the summary to the console.
4. **Exporters**: Create a PPTX with one slide per key section.
5. **Web Interface**: Enable file uploads and result downloads.

---

## Project Roadmap

To guide development and your learning, the project is divided into these phases:

### Phase 0: Environment Setup
- Choose the programming language: **Python**.
- Set up a virtual environment (`venv`) and manage dependencies with `requirements.txt`.
- Initialize the repository structure (`src/`, `input/`, `output/`, `docs/`).

### Phase 1: Text Extraction
- Implement PDF extraction with `pdfplumber` or `PyMuPDF`.
- Implement DOCX extraction with `python-docx`.
- Validate extraction on sample documents.

### Phase 2: Preprocessing
- Clean text: remove extra whitespace, special characters, and normalize.
- Tokenize and segment into headings, subheadings, and paragraphs using **spaCy** or **NLTK**.
- Create reusable functions for structuring content.

### Phase 3: Summarization
- Integrate a Hugging Face model (e.g., **T5-small** or quantized **PEGASUS**).
- Build an inference pipeline handling input lengths, batching, and memory limits.
- Evaluate summary quality against manual extracts.

### Phase 4: Exporters
- Generate **DOCX** files with structured notes using **python-docx**.
- Generate **PPTX** slides for each key section using **python-pptx**.
- Ensure consistent formatting and styling.

### Phase 5: User Interface
- Develop a user-friendly **CLI** with `argparse` or `click`.
- Build a **Web UI** with **Streamlit** or **Gradio**.
- Coordinate module calls for extraction, preprocessing, summarization, and exporting.

### Phase 6: Testing and CI/CD
- Write unit and integration tests for each component.
- Configure **GitHub Actions** for linting, testing, and building.
- Optionally deploy a demo on Streamlit Community Cloud or Heroku.

### Phase 7: Documentation and Examples
- Add usage examples in `docs/` with screenshots.
- Document the internal API and CLI commands in `README.md`.
- Provide a `CONTRIBUTING.md` guide and roadmap for future collaborators.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute to this project.

