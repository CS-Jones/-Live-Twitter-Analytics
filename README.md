# Live Twitter Analytics & Visualisation Dashboard 🐦📊

A full-stack asynchronous data analytics platform designed to collect live streaming tweets via the Twitter API, execute real-time natural language processing (NLP) sentiment scoring, and pipe data natively to dynamic frontend visualisations.

## 📂 Repository Architecture

The project is segmented into distinct logic directories handling data ingestion, sentiment computation, and graphical layout layers:

```text
📁 Project-Python-Scripts--master/
│
├── 📁 API Graph/                  # 🌐 GRAPH RENDERING & FRONTEND ASSETS
│   ├── 📄 graph.html              # Core frontend canvas embedding D3/graph matrices
│   ├── 📄 api.py                  # Flask backend broker piping data to frontend nodes
│   └── 📄 getAll.js               # jQuery handlers dispatching asynchronous requests
│
├── 📁 LiveAnalysis/               # ⚡ REAL-TIME STREAM PROCESSING LAYER
│   ├── 📄 liveAnalysis.py         # Tweepy listener streaming live matching keyword fields
│   ├── 📄 scatterTweets.py        # Generates static Matplotlib plots of text weights
│   └── 🖼️ plot_image.png          # Exported snapshot of structural cluster arrays
│
├── 📄 TFIDF.py                    # 🧮 Term Frequency-Inverse Document Frequency weight calculator
├── 📄 dataCollection.py          # Standalone batch data aggregation routine
├── 📄 testTextBlob.py             # NLP baseline validating polarity and subjectivity indices
└── 📄 100tweets.json              # Mock raw payload dataset used for local execution pipelines
```

## 🚀 Core Features

* **Live Asynchronous Streaming:** Integrates `Tweepy` streaming blocks to open high-throughput connection pipelines capturing live match filters.
* **Algorithmic Sentiment Profiling:** Leverages the `TextBlob` library to calculate natural language scores, tracking conversational metrics across *Polarity* and *Subjectivity* matrices.
* **Decoupled Data Brokers:** Uses a lightweight `Flask` framework configuration (`api.py`) to map unstructured local system objects safely into clean REST API JSON arrays.
* **Interactive Frontend Visuals:** Renders beautiful HTML canvas layouts driven by `jQuery` AJAX workers to plot network nodes and dataset distributions without page reloads.

## 🛠️ Tech Stack & Requirements

### Backend Requirements
* **Language:** Python 3.8+
* **Core Libraries:**
  * `tweepy` - Official stream controller interfacing with the Twitter Developer API.
  * `flask` / `flask-cors` - Broker engine serving dataset parameters to frontends.
  * `textblob` - Main NLP analyzer determining content sentiment characteristics.
  * `pandas` / `numpy` / `matplotlib` - Analytical grid sorting and static image generation.

### Frontend Requirements
* **Libraries:** jQuery 3.3.1, modern web browsers supporting canvas rendering layouts.

## ⚙️ Compilation & Deployment Instructions

### 1. Build and Configure Virtual Environment
Clone the repository using git commands locally on your machine and set up a sandbox environment:
```bash
git clone https://github.com
cd Project-Python-Scripts
python3 -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 2. Install Project Dependencies
Use `pip` to grab required third-party data processing and text blob library architectures:
```bash
pip install tweepy flask flask-cors textblob pandas numpy matplotlib
```

### 3. Initialize API Credentials
Create a file named `credentials.py` or export your Twitter Developer Portal tokens to your local system environment variables:
```python
# API configuration tokens mapping
CONSUMER_KEY = "your_consumer_key"
CONSUMER_SECRET = "your_consumer_secret"
ACCESS_TOKEN = "your_access_token"
ACCESS_TOKEN_SECRET = "your_access_token_secret"
```

### 4. Run the Processing Engine
Launch the streaming worker to fetch live payloads and populate local cache matrices:
```bash
python LiveAnalysis/liveAnalysis.py
```

### 5. Launch the Flask API Broker
In a separate terminal workspace, spin up the API web server layer:
```bash
python "API Graph/api.py"
```

### 6. Open Frontend Visualizations
Simply execute or host `API Graph/graph.html` on a local live server extension inside your browser window context to observe structural real-time graph components mapping automatically.

## 🗺️ Roadmap & Unfinished Features

* [ ] **Migrate to Twitter API v2:** Upgrade streaming listeners from deprecated v1.1 endpoint endpoints to compliant v2 structures.
* [ ] **Add Async Socket.io:** Replace traditional jQuery AJAX polling mechanisms with live web socket loops for smooth rendering.
* [ ] **Secure Secret Handling:** Refactor exposed hardcoded data variables out of scripts into `.env` configuration matrices.

## 📄 License

This repository is open-source software and available under the [MIT License](LICENSE).
