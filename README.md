# Movie Recommendation System

Flask-based movie recommendation system using a pre-trained sentiment model, content-based similarity, TMDB movie details, and IMDb reviews.

## Run locally on Windows

### 1. Open the project in VS Code
Open this folder (the folder containing `app.py`) in VS Code.

### 2. Create a virtual environment
Use Python 3.10 or 3.11 for best compatibility with the included scikit-learn pickle files.

```powershell
py -3.11 -m venv .venv
.venv\Scripts\activate
```

If `py -3.11` is unavailable, use your installed Python version and create the environment with `python -m venv .venv`.

### 3. Install dependencies

```powershell
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure TMDB
The UI uses The Movie Database (TMDB) API to fetch posters, cast, ratings, genres, etc.

Copy `.env.example` to `.env` and put your TMDB API key in it:

```text
TMDB_API_KEY=your_tmdb_api_key_here
```

Do not commit `.env` to GitHub.

### 5. Start the application

```powershell
python app.py
```

Then open `http://127.0.0.1:5000` in your browser.

## Important

- The original project contained hard-coded paths pointing to another computer. Those paths have been replaced with project-relative paths.
- The model files are already included in `Artifacts/`; you do not need to retrain the model.
- If TMDB requests fail, verify that the key in `.env` is valid.
- IMDb review scraping depends on IMDb's current website behavior and may fail if IMDb changes its page structure or blocks the request.
