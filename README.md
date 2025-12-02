Deployes link (https://heart-disease-prediction-l69z.onrender.com/)

Heart Disease Streamlit App

This repository contains a Streamlit app (`web.py`) for predicting heart disease risk using a saved KNN model and preprocessor files.

Quick checklist before deploying
- Ensure these files are present in the repo root: `web.py`, `KNN_heart.pkl`, `scaler.pkl`, `columns.pkl`, and `requirements.txt`.
- If model files are large (>100 MB), use Git LFS or host them remotely and update `web.py` to download them at runtime.

Deploy to Streamlit Community Cloud (recommended)
1. Push your project to a GitHub repository.
2. Sign in at https://share.streamlit.io with your GitHub account.
3. Click "New app" → select the repo, branch (`main`) and set the main file path to `web.py` → Deploy.

Notes for Streamlit Cloud
- No additional configuration is required if your files are in the repo root and `requirements.txt` is present.
- If you need environment secrets (API keys, etc.), set them in the Streamlit Cloud app settings.

Deploy to other hosts (Render, Railway, Docker)
- For hosts that set a port via an environment variable (`$PORT`) you may need to start Streamlit with: `streamlit run web.py --server.port $PORT --server.headless true`.
- For Docker deployment, create a `Dockerfile` and expose the required port; install Python dependencies from `requirements.txt`.

Push to GitHub (PowerShell example)
```powershell
cd "c:\Users\hp\Desktop\Heart disease"
git init
git add .
git commit -m "Initial commit: Streamlit heart app"
git branch -M main
# Create a repo on GitHub, then run (replace URL):
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

If you'd like, I can:
- Help create the `git` repo and push these changes.
- Add a `Dockerfile` or a Render-specific `start` command.
- Walk you through Streamlit Cloud deployment step-by-step.
