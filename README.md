# HousingHub – Machine Learning API

This repository is my **personal showcase copy** of the original HousingHub project. The full team repository is here: 

👉 Original team repo: https://github.com/kaylals/HousingHub 

In this personal repo, I focus on the **backend machine learning APIs** that power the housing price forecasting features. 

--- ## My Role In the original team project, my main responsibility was to: 

- Take existing machine learning models (e.g., N-Beats for short-term forecasts and XGBoost for long-term forecasts), 
- Wrap them into **Flask-based HTTP APIs**,
- Handle data loading and preprocessing inside the API,
- Define the request/response schema so the frontend can consume model predictions, 
- Expose endpoints that return prediction plots and values. 

In short: **I turned the ML model outputs into a reusable backend API layer** that other parts of the system (frontend / dashboard) can call. 

--- ## Running the Machine Learning API Locally

### 1. Clone this repository
```bash
git clone https://github.com/leyulunna/housinghub_backend.git
cd HousingHub
```

### 2. Create & activate virtual environment

If you don’t already have a .venv:
Activate it (macOS / Linux):
```bash 
python3 -m venv .venv 
source .venv/bin/activate
```

(If you are on Windows PowerShell, it would be:)
```bash 
.\.venv\Scripts\Activate 
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Install dependencies
From the project root:

```bash
python3 code/machine_learning/app.py
```

This will start the Flask server (default port: 5000).
You can then call the API endpoints for:

- Short-term predictions (N-Beats model)
- Long-term predictions (XGBoost model)

Details are inside:

- code/machine_learning/app.py
- code/machine_learning/n_beats_day_2.py
- code/machine_learning/predict_xgboost.py