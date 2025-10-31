 AI News Bot — AI-Powered News Categorization System

Run AI News Bot on Target Machine (Offline/Local Setup)

This guide explains how to set up and run the AI News Bot, a smart system that classifies and displays news articles into categories such as Politics, Sports, Technology, Entertainment, Health, and Weather using AI and NLP techniques.


What is AI News Bot?

AI News Bot is an AI-driven text classification project that uses Natural Language Processing (NLP) and Machine Learning to automatically categorize news headlines or articles.  
It can be configured to work offline (with local datasets) or online (by fetching live news from APIs).


Prerequisites

Before running the project, ensure you have the following installed:

- Python 3.8+
-  Pip / Virtual Environment
-  Libraries (specified in `requirements.txt`):
  -  scikit-learn
  -  pandas
  -  numpy
  -  nltk
  -  flask or fastapi
  -  requests
  - beautifulsoup4 (optional, for web scraping)


Folder Structure

Ensure your folder structure looks like this:
      AI-News-Bot/
- app.py # Main application file
- requirements.txt # All dependencies
- model/
- news_classifier.pkl # Trained ML/NLP model
- vectorizer.pkl # TF-IDF or CountVectorizer
- dataset/
- news.csv # Dataset containing news text and labels
- static/ # (Optional) For web UI assets
- templates/ # (Optional) For HTML pages
- README.md

Step 1: Create Virtual Environment (Optional)
```bash
python -m venv venv
venv\Scripts\activate    # On Windows
source venv/bin/activate # On Mac/Linux

Step 2: Install Dependencies
pip install -r requirements.txt

Step 3: Run the Application
python app.py
You’ll see output similar to:
Running on http://127.0.0.1:5000

Access the Application
Open your browser and go to:
   http://localhost:5000

Usage
1. Enter or Upload news headline/text
2. The system processes and vectorizes the input
3. AI model predicts the category
4. Result displayed as: Politics, Sports, Technology, etc.

Offline Functionality
•	Works completely offline if using a local dataset and trained model
•	No API keys or external services required
•	Uses local preprocessing and classification logic

Notes
•	The first run may take a few seconds as the model loads.
•	To re-train with your own data, replace dataset/news.csv and run the training script (if provided).
•	For live news integration, connect to NewsAPI or Google News RSS (optional).
