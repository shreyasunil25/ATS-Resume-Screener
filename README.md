# Smart ATS Resume Screener 📄

Upload your resume and paste a job description to get an AI-powered ATS 
compatibility analysis — built with Google Gemini.

## Features
- Resume review: strengths and weaknesses against the JD
- ATS match score: percentage match + missing keywords + final verdict
- Accepts PDF resumes
- Powered by Google Gemini 1.5 Flash

## Tech Stack
- Python, Streamlit
- Google Gemini API
- pdf2image, Pillow

## Setup

1. Install system dependency (poppler):
   - Mac: brew install poppler
   - Linux: sudo apt-get install poppler-utils

2. Install Python packages:
   pip install -r requirements.txt

3. Add your API key — create a .env file:
   GOOGLE_API_KEY=your_key_here

4. Run:
   streamlit run ats_screener.py

## How It Works
The app converts the uploaded PDF to an image and sends it along with 
the job description to Gemini's vision model. Gemini evaluates alignment, 
returns a match percentage, lists missing keywords, and provides a 
professional HR-style assessment.
