
#  News CLI — Summarize & Analyze News with Gemini AI

**News CLI** is a command-line tool for fetching, summarizing, and bias-classifying news articles using Gemini 1.5 Flash. It connects to a MongoDB database for article storage and leverages AI to help users consume news faster and smarter.

---

##  Features

-  Fetch top headlines, detailed articles, and breaking news
-  AI-powered article summarization with Gemini 1.5
-  Detects bias levels: Neutral, Mildly Biased, Strongly Biased
-  Stores all articles in MongoDB for persistent use
-  User-friendly command-line interface

---

##  Project Structure

```
 News CLI
├── main.py                # CLI interface
├── db.py                  # MongoDB connection & collections
├── summarizer.py          # Gemini-based summarizer
├── bias_classifier.py     # Gemini-based bias classification
├── .env                   # Environment variables (not included)
```

---

##  Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/news-cli.git
cd news-cli
```

### 2. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
MONGODB_URI=your_mongodb_uri
GEMINI_API_KEY=your_google_generative_ai_api_key
```

---

### 3. Install Dependencies

It's recommended to use a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

> Dependencies include:
> - `google-generativeai`
> - `pymongo`
> - `newspaper3k`
> - `python-dotenv`

---

##  How to Use

Run the app:
```bash
python main.py
```

Available commands:
- `1` → Get top headlines
- `2` → Get detailed articles
- `3` → Get breaking headlines
- `4` → Summarize selected article
- `5` → Classify selected article for bias
- `6` → Exit

---

##  AI Integration

- **Gemini 1.5 Flash** used for both summarization and bias detection
- Summaries are concise, 4–6 bullet points
- Bias detection outputs a classification + explanation

---

##  MongoDB Collections

- `top_headlines`
- `all_articles`
- `breaking_headlines`

Articles fetched are stored and reused for summarization and analysis.

---

##  License

MIT License. Feel free to fork, modify, and contribute.

---

##  Credits

- [Google Generative AI](https://ai.google.dev/)
- [newspaper3k](https://github.com/codelucas/newspaper)
- [pymongo](https://pymongo.readthedocs.io/)
