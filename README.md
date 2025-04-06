# SHL Assessment Recommendation System

A machine learning-powered recommendation system that suggests the most suitable SHL assessments based on job descriptions or job posting URLs.

## Features

- Recommends SHL assessments using semantic similarity
- Supports both text input and URL parsing
- Displays results with key assessment details
- Modern, responsive web interface

## System Architecture

```
shl-recommender/
├── backend/               # Flask API server
│   ├── app.py             # Main application
│   ├── recommendation_engine.py  # ML recommendation logic
│   └── data/
│       └── shl_assessments.json  # Assessment database
└── frontend/              # Web interface
    ├── index.html         # Main page
    └── api.js             # Client-side JavaScript
```

## Prerequisites

- Python 3.10+
- Google Generative AI API key
- Node.js (for optional frontend development)

## Installation

1. Clone the repository
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. Set your Google API key as an environment variable:
   ```bash
   export GOOGLE_API_KEY='your-api-key'
   ```

## Running the Application

1. Start the backend server:
   ```bash
   cd shl-recommender/backend
   python app.py
   ```

2. Start the frontend server (in a new terminal):
   ```bash
   cd shl-recommender/frontend
   python3 -m http.server 8000
   ```

3. Access the application at: http://localhost:8000

## Usage

1. Enter either:
   - A job description in the text area
   - Or a URL to a job posting
2. Click "Get Recommendations"
3. View the recommended assessments in the results table

## API Endpoints

- `POST /api/recommend` - Accepts JSON with either `text` or `url` field
- Returns JSON array of recommended assessments

## Future Enhancements

- User authentication
- Assessment comparison feature
- Integration with SHL's API
- More detailed assessment information

