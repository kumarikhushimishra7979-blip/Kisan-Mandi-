# Kisan-Mandi-
Audio-first, multilingual ML app forecasting APMC mandi prices for Indian farmers. Features voice queries, regional audio readouts, and intuitive visual Hold/Sell signals. Powered by time-series models for crops like maize and paddy in Bihar, built using FastAPI, Streamlit, and XGBoost.
# 🌾 Kisan Mandi Bhav Predictor & Voice Advisory Assistant

An audio-first, multilingual, and visual web application designed to forecast APMC agricultural commodity prices and provide actionable market guidance for farmers in rural India.

---

## 🚀 About the Project
Smallholder farmers across India often face severe price volatility when selling produce at local mandis due to a lack of advance market visibility and complex, English-heavy web interfaces. 

**Kisan Mandi Bhav Predictor** bridges this gap by combining time-series machine learning forecasting with a **voice-first, icon-driven, and multilingual** user interface. It translates complex price trajectories into simple, actionable visual and audio signals (Hold vs. Sell) in regional languages.

---

## ✨ Key Features

* **🗣️ Voice-First Input (Speech-to-Text):** Farmers can tap a large microphone button and speak queries naturally in Hindi, regional dialects, or English (e.g., *"Aaj makka ka bhav kya hai?"*).
* **🔊 Multilingual Audio Readouts (Text-to-Speech):** Automatic audio playback explains price trends and market advice aloud.
* **🟢 Color-Coded Visual Guidance:** Replaces dense data tables with intuitive vector icons and color cards:
  * 🟢 **Green:** Prices rising $\rightarrow$ *Hold stock.*
  * 🔴 **Red:** Prices falling $\rightarrow$ *Sell immediately.*
  * 🟡 **Yellow:** Stable pricing.
* **📈 ML Time-Series Forecasting:** Powered by regression models tracking historical APMC mandi transaction records with lag features and rolling averages.
* **🌍 Regional Scope:** Tailored for core staple crops (Maize, Paddy, Wheat) across regional markets like Gulabbagh (Purnea, Bihar).

---

## 🛠️ Technology Stack

* **Frontend & Interactive UI:** Streamlit
* **Machine Learning Core:** Python, Pandas, NumPy, Scikit-Learn, XGBoost
* **Voice & Multilingual Layer:** Web Speech API / gTTS (Google Text-to-Speech)
* **Backend API:** FastAPI & Uvicorn

---

## 📁 Project Directory Structure

```text
mandi-price-prediction/
├── data/
│   └── agmarknet_data.csv          # Historical mandi price records
├── models/
│   └── xgboost_maize_gulabbagh.joblib # Trained machine learning model artifact
├── src/
│   ├── preprocess.py               # Data cleaning & lag feature engineering
│   ├── train.py                    # Model training & metric evaluation script
│   └── inference.py                # Recursive 7-day forecasting & advisory engine
├── app.py                          # FastAPI backend endpoints
├── streamlit_app.py                # Streamlit multilingual visual frontend
├── requirements.txt                # Project dependencies
└── README.md                       # Project documentation
