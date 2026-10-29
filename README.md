# 🎓 Smart School AI

A beginner-friendly School Management web application built with Python and Streamlit.

## Features
- Dashboard with school statistics
- Register, search, and remove student records
- Attendance tracking
- Marks entry and automatic percentage/grade calculation
- Download student, attendance, and result data as CSV
- Optional AI Study Assistant (requires an OpenAI API key)
- Responsive Streamlit interface

## Run locally (Windows)

1. Install Python 3.10 or newer from https://www.python.org/downloads/
2. Extract this project folder.
3. Open Command Prompt in this folder.
4. Create a virtual environment:

   ```bash
   py -m venv .venv
   .venv\Scripts\activate
   ```

5. Install packages:

   ```bash
   pip install -r requirements.txt
   ```

6. Start the app:

   ```bash
   streamlit run app.py
   ```

7. Open the local URL shown in the terminal (usually http://localhost:8501).

## Upload this project to GitHub

1. Sign in at https://github.com/
2. Click **New repository**.
3. Name it `smart-school-ai`; choose Public if you want others to see it.
4. Create the repository. Do not add a README if you are uploading this folder's README.
5. In Command Prompt, open this folder and run:

   ```bash
   git init
   git add .
   git commit -m "Initial Smart School AI app"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/smart-school-ai.git
   git push -u origin main
   ```

   Replace `YOUR-USERNAME` with your GitHub username. Git may ask you to sign in.

If Git is not installed, install it from https://git-scm.com/downloads and reopen Command Prompt.

## Deploy free on Streamlit Community Cloud

1. Push the files to GitHub using the instructions above.
2. Open https://share.streamlit.io/ and sign in with GitHub.
3. Click **Create app** / **Deploy an app**.
4. Select the `smart-school-ai` repository, branch `main`, and main file path `app.py`.
5. Click **Deploy** and wait for the build to finish.
6. Streamlit will provide a public URL for your app.

## Optional AI setup

The AI Study Assistant works in demo mode without an API key. To enable live AI, create an API key through your AI provider and add it in Streamlit Community Cloud under **App settings → Secrets**:

```toml
OPENAI_API_KEY = "your-api-key"
```

The current app also accepts a key in the AI page. Never commit keys or secrets to GitHub. API usage may incur charges.

## Important limitations

This is a demo/educational starter app. Data is stored in Streamlit session state and may be lost when a session resets or the app restarts. It has no login system and should not be used to store real confidential student information. For production use, add authentication, permissions, persistent database storage, backups, and privacy/security controls.
