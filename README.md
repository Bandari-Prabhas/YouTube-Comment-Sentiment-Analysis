# YouTube Comment Sentiment Analyzer

A full-stack Python web application that fetches YouTube comments for a given video, analyzes their sentiment using state-of-the-art NLP models, generates a summary of the comments, and displays detailed insights. It utilizes both pre-trained transformer models and Google's Generative AI (Gemini) API for summarization, along with a backup neural network for sentiment analysis.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [API Keys & Configuration](#api-keys--configuration)
- [How to Run the Program](#how-to-run-the-program)
- [How the Program Works](#how-the-program-works)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Features

- **YouTube Comments Retrieval:**  
  Fetches up to 200 comments from a specified YouTube video using the YouTube Data API.

- **Sentiment Classification:**  
  Uses Facebook’s `bart-large-mnli` model in a zero-shot classification pipeline to categorize comments (e.g., positive, negative, neutral, suggestions/feedback, spam/promotional).

- **Summarization:**  
  Generates a detailed summary of the comments by leveraging the Gemini API from Google Generative AI. If the Gemini API call fails, a fallback summarizer (based on Hugging Face's `sshleifer/distilbart-cnn-12-6`) is used.

- **Backup Sentiment Analysis:**  
  A custom Keras-based neural network (trained on Amazon reviews data) serves as an additional backup for sentiment classification.

- **Downloadable Results:**  
  Provides a CSV download of the analyzed results for further review or reporting.

## Installation

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone <repository_url>
cd youtube-comment-sentiment-analyzer


