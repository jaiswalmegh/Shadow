# 🛡️ SHADOW
### AI-Powered Campus Intelligence & Anomaly Detection System

SHADOW is an AI-powered campus intelligence platform designed to identify unusual operational patterns, correlate signals from multiple data sources, and generate evidence-based insights for campus monitoring and investigation.

The system analyzes campus datasets such as attendance, complaints, facility usage, helpdesk records, and feedback to detect anomalies and identify potential operational or network-related issues.

## 🚀 Key Features

- **Multi-Source Data Analysis:** Processes data from five different campus data sources.
- **Data Normalization:** Converts raw datasets into a consistent format for analysis.
- **Anomaly Detection:** Identifies unusual changes in campus activity using historical baselines.
- **Signal Correlation:** Connects abnormal signals across independent sources to identify potential issues.
- **Confidence Scoring:** Evaluates the strength of supporting evidence.
- **AI-Powered Explanations:** Generates understandable explanations for detected issues.
- **Investigation Engine:** Provides issue summaries, supporting evidence, and recommendations.
- **Interactive Dashboard:** Presents campus intelligence through a React-based interface.
- **Location-Based Analysis:** Helps identify potential issues across different campus locations.

## 🧠 How SHADOW Works

SHADOW follows a structured data intelligence pipeline:

1. **Data Ingestion:** Loads attendance, complaints, facility usage, helpdesk, and feedback datasets.
2. **Data Normalization:** Standardizes data into a unified structure.
3. **Anomaly Detection:** Compares recent observations against historical baselines.
4. **Signal Correlation:** Identifies relationships between abnormal signals.
5. **Confidence Scoring:** Evaluates supporting signals and independent evidence sources.
6. **AI Analysis:** Generates explanations and investigation recommendations.
7. **Dashboard Visualization:** Displays findings for easier analysis and investigation.

## 🛠️ Tech Stack

**Backend**
- Python
- Flask
- Flask-CORS
- Pandas
- NumPy

**Frontend**
- React
- Vite
- JavaScript
- HTML5
- CSS3
- Recharts

**Data Storage and Processing**
- CSV datasets
- SQL schema and database utilities
- Historical baseline analysis

## 📂 Project Structure

```text
SHADOW/
├── backend/
│   ├── ai/
│   │   └── analyzer.py
│   ├── data/
│   │   ├── attendance.csv
│   │   ├── complaints.csv
│   │   ├── facility_usage.csv
│   │   ├── feedback.csv
│   │   └── helpdesk.csv
│   ├── database/
│   │   ├── db.py
│   │   └── schema.sql
│   ├── engine/
│   │   ├── anomaly.py
│   │   ├── confidence.py
│   │   ├── correlation.py
│   │   ├── detector.py
│   │   └── normalizer.py
│   ├── routes/
│   │   └── investigation.py
│   ├── app.py
│   └── config.py
├── frontend/
│   ├── src/
│   ├── index.html
│   └── package.json
└── README.md
```

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.10 or later
- Node.js and npm
- Git

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd shadow
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your GitHub repository URL.

### 2. Install Backend Dependencies

From the project root, create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install the required packages:

```bash
pip install flask flask-cors pandas numpy
```

### 3. Start the Backend

From the project root, run:

```bash
python backend/app.py
```

The Flask server will start using the configured local development address.

### 4. Start the Frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed by Vite in your browser.

### 5. Build the Frontend

To build the frontend for serving through Flask:

```bash
npm run build
```

The production build is generated in the `frontend/dist` directory.

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Serves the frontend or backend status information |
| GET | `/api/health` | Checks backend health |
| GET | `/api/investigation/` | Retrieves analyzed campus investigations |
| GET | `/api/investigation/<location>` | Retrieves investigations for a specific location |

### Example API Request

```bash
curl http://127.0.0.1:5000/api/health
```

To retrieve investigations:

```bash
curl http://127.0.0.1:5000/api/investigation/
```

## 📊 Anomaly Severity Classification

SHADOW classifies signal deviations using percentage changes from historical baselines.

| Severity | Percentage Change |
|---|---:|
| NORMAL | Below 20% |
| WATCH | 20% to below 50% |
| ANOMALY | 50% to below 100% |
| SEVERE | 100% or above |

These thresholds are configurable and can be adjusted according to the use case.

## 🎯 Potential Applications

- Campus operational monitoring
- Network infrastructure issue detection
- Attendance pattern analysis
- Facility usage monitoring
- Complaint and feedback analysis
- Evidence-based campus investigations

## 🔮 Future Scope

- Machine learning-based anomaly detection
- Real-time monitoring and alert generation
- Advanced graph-based relationship analysis
- Interactive investigation timelines
- Improved explainability and model evaluation
- Automated analytical report generation

## ⚠️ Disclaimer

SHADOW identifies unusual patterns and potential issues based on available data. Its findings are analytical indicators, not definitive proof of a problem. Results should be validated using reliable source data and appropriate human review.

## 👨‍💻 Project Status

SHADOW is a campus intelligence and anomaly detection project combining data analytics, backend processing, signal correlation, and interactive visualization.

---

**SHADOW | Detect Patterns. Connect Signals. Reveal Insights.** 🛡️
