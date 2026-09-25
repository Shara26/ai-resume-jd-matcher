# AI-Powered Resume–JD Matcher

An AI-powered ATS-style system that analyzes resumes against job descriptions and generates a match score with detailed reasoning.

## Overview

The system automates the initial resume screening process by extracting relevant candidate information from resumes and comparing it with the requirements of a given job description using Large Language Models (LLMs).

It supports PDF and DOCX resumes and uses structured LLM outputs to produce consistent and reliable candidate evaluations.

## Key Features

- **Resume Parsing:** Extracts text and structured information from PDF and DOCX resumes, including data from complex tables.
- **LLM-Based Analysis:** Uses the Groq API to analyze resumes and job descriptions.
- **Structured Outputs:** Uses Pydantic schemas and JSON-mode outputs to validate and maintain consistent LLM responses.
- **Candidate Matching:** Compares candidate skills, experience, education, and other relevant information with job requirements.
- **Match Scoring:** Generates a score from **0–100** representing the overall resume–job description match.
- **Detailed Evaluation:** Identifies candidate strengths, weaknesses, and provides reasoning behind the match score.
- **Rate Limiting:** Implements controlled API requests to avoid excessive calls and support processing of multiple documents.

## System Workflow

```text
Resume (PDF / DOCX)
        ↓
Document Parsing
        ↓
Text Extraction
        ↓
Structured Information Extraction
        ↓
Pydantic Validation
        ↓
Job Description Analysis
        ↓
Resume–JD Comparison
        ↓
Match Score (0–100)
        ↓
Strengths + Weaknesses + Reasoning
