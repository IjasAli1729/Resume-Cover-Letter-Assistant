# Resume-CoverLetter-Agent

An automated, stateful workflow built with **LangGraph** that generates high-quality resume summaries and personalized cover letters based on specific job descriptions.

## 🏗 Workflow Overview
This project uses a directed graph to orchestrate document generation:
* **Resume Summarizer**: Analyzes a job description to extract key requirements and rephrase them into a strong, applicant-focused resume summary.
* **Cover Letter Writer**: Integrates the generated resume summary with the job requirements to draft a tailored cover letter.

## 🚀 Key Features
* **Stateful Orchestration**: Uses `ChainState` to maintain context between document generation steps.
* **LLM Integration**: Powered by Google’s `gemini-2.5-flash` model for intelligent text synthesis.
* **Modular Pipeline**: Easily extendable to include nodes for interview preparation or LinkedIn optimization.

## 🛠 Prerequisites
* Python 3.12+
* `langgraph`, `langchain-google-genai`, `python-dotenv`

## ⚙️ Installation
1. Clone this repository: `git clone <your-repo-url>`
2. Install dependencies: `pip install -r requirements.txt`
3. Add your `GOOGLE_API_KEY` to a `.env` file.

## 💡 Usage
```python
input_state = {
    "job_discription": "Your job description text here..."
}
result = app.invoke(input_state)
print(result['cover_letter'])
