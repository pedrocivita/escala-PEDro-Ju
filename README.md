# PEDro Scale Article Analyzer

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.35.0-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![Google AI](https://img.shields.io/badge/Google%20AI-Gemini-4285F4?logo=google&logoColor=white)](https://ai.google.dev/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An intelligent web application that automates the evaluation of scientific articles using the PEDro (Physiotherapy Evidence Database) scale. Developed as part of the Computer Engineering program at Insper, this tool leverages Google's Gemini AI to provide comprehensive methodological quality assessments of clinical trials and research papers.

## Overview

The PEDro Scale Article Analyzer is a sophisticated tool designed to assist researchers, healthcare professionals, and students in evaluating the methodological quality of scientific articles. By combining PDF text extraction with advanced AI analysis, the application provides detailed assessments based on the internationally recognized PEDro scale criteria.

### Key Features

- **Automated PDF Processing**: Seamless extraction of text content from research articles
- **AI-Powered Analysis**: Integration with Google's Gemini 1.5 Flash model for intelligent evaluation
- **Comprehensive PEDro Scoring**: Evaluation across all 11 criteria of the PEDro scale
- **Detailed Justifications**: Evidence-based explanations for each criterion assessment
- **Reliability Classification**: Automatic categorization into low, moderate, or high reliability
- **Interactive Interface**: User-friendly Streamlit-based web application
- **Secure API Integration**: Protected API key management for Google AI Studio

## The PEDro Scale

The PEDro (Physiotherapy Evidence Database) scale is a validated tool for assessing the methodological quality of randomized controlled trials. It evaluates 11 key criteria:

1. Eligibility criteria specification
2. Random allocation
3. Concealed allocation
4. Baseline similarity
5. Subject blinding
6. Therapist blinding
7. Assessor blinding
8. Adequate follow-up
9. Intention-to-treat analysis
10. Between-group statistical comparisons
11. Point measures and variability

The scale produces a score from 0 to 10 (criterion 1 is not scored), which is then categorized into reliability levels:
- **0-3**: Low reliability
- **4-6**: Moderate reliability
- **7-10**: High reliability

## Prerequisites

- Python 3.8 or higher
- Google AI Studio API key (free tier available)
- Internet connection for API calls

## Installation

1. Clone the repository:
```bash
git clone https://github.com/pedrocivita/escala-PEDro-Ju.git
cd escala-PEDro-Ju
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Start the Streamlit application:
```bash
streamlit run app.py
```

2. Open your web browser and navigate to the provided local URL (typically `http://localhost:8501`)

3. Obtain a Google AI Studio API key:
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Click "Create API key"
   - Copy the generated key

4. In the application sidebar:
   - Enter your Google AI Studio API key
   - Upload a PDF file of the scientific article you want to analyze
   - Click "Analisar Artigo" (Analyze Article)

5. Review the comprehensive analysis including:
   - Individual criterion assessments with justifications
   - Overall PEDro score
   - Reliability classification
   - Summary of findings and clinical applicability

## Project Structure

```
escala-PEDro-Ju/
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
├── README.md          # Project documentation
└── .gitignore         # Git ignore rules
```

## Technical Implementation

### Technologies Used

- **Streamlit**: Web application framework for rapid development
- **PyPDF2**: PDF text extraction and processing
- **Requests**: HTTP library for API communication
- **Google Gemini AI**: Advanced language model for article analysis

### Architecture

The application follows a modular design:

1. **PDF Processing Module**: Handles file upload and text extraction with a 28,000 character limit to ensure optimal API performance and stay within token constraints
2. **AI Analysis Module**: Constructs detailed prompts and manages communication with Google's Gemini API
3. **User Interface Module**: Provides an intuitive Streamlit-based interface for user interaction

### API Integration

The application uses Google's Generative Language API (Gemini 1.5 Flash) with:
- RESTful API endpoints
- JSON payload formatting
- Robust error handling and user feedback
- Secure API key management

## Academic Context

This project was developed as part of the Computer Engineering curriculum at **Insper - Instituto de Ensino e Pesquisa**, demonstrating the practical application of artificial intelligence in healthcare and research methodology assessment.

## Author

**Pedro Civita**

- Email: [pedrobc@al.insper.edu.br](mailto:pedrobc@al.insper.edu.br)
- Email: [pedrocivita1@gmail.com](mailto:pedrocivita1@gmail.com)
- LinkedIn: [linkedin.com/in/pedrocivita](https://www.linkedin.com/in/pedrocivita)
- GitHub: [@pedrocivita](https://github.com/pedrocivita)

## Contributing

This project is part of an academic portfolio. Suggestions and feedback are welcome through GitHub issues or direct contact.

## License

This project is available under the MIT License. See the LICENSE file for more details.

## Acknowledgments

- **Insper - Instituto de Ensino e Pesquisa** for the academic framework
- **Julia Takieddine** for collaboration and domain expertise in psychology and neuropsychology
- **Google AI** for providing access to the Gemini API
- The **PEDro Scale** developers for creating a robust methodology assessment tool

---

*Developed with precision and care as part of the Insper Computer Engineering program*
