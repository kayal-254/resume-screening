# AI Resume Screening System

A professional AI-powered tool for HR professionals to rank resumes against a job description using Machine Learning (TF-IDF + Cosine Similarity) and NLP.

## Features
- **File Support**: Extract text from **PDF** and **DOCX** files.
- **NLP Processing**: Uses **spaCy** for intelligent text preprocessing (stopword removal, lemmatization).
- **ML Scoring**: Calculates similarity scores (0-100%) using **Scikit-Learn**.
- **Modern UI**: Premium dark-mode interface with glassmorphism effects.
- **Database**: SQLite integration to store job descriptions and resume rankings.

## Project Structure
```text
resume_screening/
├── app.py           # Flask routes and logic
├── models.py        # Database schema
├── utils.py         # NLP & ML utility functions
├── templates/       # Jinja2 HTML templates
├── static/          # CSS and Assets
├── uploads/         # Temporary storage for resumes
└── requirements.txt  # Dependencies
```

## Quick Start (Recommended)
You can use the provided `run.py` script to automatically install dependencies, download NLP models, and start the server.

```bash
python run.py
```

## Manual Installation
If you prefer manual setup:

1. **Install Dependencies**:
   ```bash
   pip install -r resume_screening/requirements.txt
   ```

2. **Download NLP Model**:
   ```bash
   python -m spacy download en_core_web_sm
   ```

3. **Run the App**:
   ```bash
   cd resume_screening
   python app.py
   ```

4. **Access the App**: Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

## Built With
- **Backend**: Python, Flask, SQLAlchemy
- **NLP**: spaCy
- **Machine Learning**: Scikit-Learn (TF-IDF, Cosine Similarity)
- **Frontend**: HTML5, CSS3 (Vanilla CSS with Premium Design)

## Future Improvements
- [ ] Implement Optical Character Recognition (OCR) for scanned PDF resumes.
- [ ] Add Email notifications for top-ranked candidates.
- [ ] Keyword highlighting in resume previews.
- [ ] Support for more file formats (RTF, TXT).