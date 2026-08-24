# AI Multi-Agent Recruitment System

A practical multi-agent AI recruitment system built with Python and Google Gemini.

The system analyzes job descriptions and candidate CVs, extracts structured information, compares skills and experience, calculates deterministic match scores, generates personalized interview questions, evaluates candidate answers, and produces a final hiring recommendation.

## Key Features

* Job description analysis
* PDF CV text extraction
* Structured CV analysis
* Skills matching and gap detection
* Deterministic weighted scoring
* Personalized interview question generation
* AI interview answer evaluation
* Final hiring recommendation
* Secure API key handling with Google Colab Secrets

## System Architecture

```text
Job Description
      |
      v
Job Analyzer Agent
      |
      v
Structured Job Data

PDF CV
  |
  v
PDF Extraction Tool
  |
  v
CV Analyzer Agent
  |
  v
Structured CV Data

Job Data + CV Data
        |
        v
  Matching Agent
        |
        v
Matched / Missing Skills
        |
        v
   Scoring Engine
        |
        v
   CV Match Score
        |
        v
   Interview Agent
        |
        v
Personalized Questions
        |
        v
Interview Evaluator
        |
        v
   Interview Score
        |
        v
 Final Hiring Report
```

## How It Works

1. The **Job Analyzer Agent** extracts required skills, experience, and education.
2. A Python PDF tool extracts text from the candidate CV.
3. The **CV Analyzer Agent** converts the CV into structured data.
4. The **Matching Agent** identifies matched skills, missing skills, and education compatibility.
5. Python calculates deterministic Skills, Experience, and Education scores.
6. The **Interview Agent** generates personalized questions based on the candidate profile and skill gaps.
7. The **Interview Evaluator Agent** evaluates candidate answers.
8. The final system combines the CV score and interview score into a hiring recommendation.

## CV Scoring

### Weights

* Skills: **40%**
* Experience: **35%**
* Education: **25%**

### Education Matching

* Exact match: **100**
* Related field: **75**
* Unrelated field: **30**

### Match Categories

* 80–100: **Strong Match**
* 70–79: **Good Match**
* 60–69: **Needs Review**
* Below 60: **Not Suitable**

## Interview Evaluation

The interview evaluator scores answers using:

* Practical Thinking: **50%**
* Clarity: **25%**
* Depth: **25%**

## Agents

* **Job Analyzer Agent**
* **CV Analyzer Agent**
* **Matching Agent**
* **Interview Agent**
* **Interview Evaluator Agent**

## Python Components

* PDF extraction tool
* Skills scoring engine
* Experience scoring engine
* Education scoring engine
* Weighted final scoring
* Hiring recommendation logic

## Tech Stack

* Python
* Google Gemini API
* Google Colab
* PyPDF
* JSON structured outputs
* Multi-Agent Architecture
* Deterministic Scoring
* Weighted Evaluation

## How to Run

1. Open `AI_Multi_Agent_Recruitment_System.ipynb` in Google Colab.

2. Add your Gemini API key to Colab Secrets as:

   `GEMINI_API_KEY`

3. Enable notebook access.

4. Run the notebook cells from top to bottom.

5. Upload a candidate CV as a PDF.

6. Provide a job description.

7. Run the full recruitment workflow.

> Never hard-code or commit your API key to GitHub.

## Project Purpose

This project was built as a hands-on exploration of multi-agent AI systems combining LLM-based reasoning with deterministic Python logic for recruitment workflows.

