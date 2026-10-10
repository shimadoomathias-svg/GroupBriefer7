# GroupBriefer

GroupBriefer is a web app for summarizing legal documents and independently checking summaries against the source for material omissions, distortions, unsupported claims, and factual/citation errors.

## Supported inputs
- PDF (text-based; scanned/image-only PDFs need OCR)
- DOCX
- TXT / Markdown

## Local setup
1. Install Python 3.12 or newer.
2. Install dependencies: `pip install -r requirements.txt`
3. Set `GROQ_API_KEY` in your environment.
4. Run: `uvicorn main:app --reload`
5. Open `http://127.0.0.1:8000`.

## Render deployment
- Runtime: Python
- Build command: `pip install -r requirements.txt`
- Start command: `uvicorn main:app --host 0.0.0.0 --port $PORT`
- Add `GROQ_API_KEY` in Render's Environment settings. Never put API keys in source files or commit them to GitHub.
- Optional variable: `GROQ_MODEL` (default `llama-3.3-70b-versatile`).

The `index.html` file must remain in the repository root beside `main.py`.

The app is not a substitute for a lawyer or primary-source verification. AI-generated summaries and evaluations can be wrong; verify important conclusions against the original document and authoritative sources.
