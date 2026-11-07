# 🚀 Token Analytics – AI Usage Monitoring & Cost Intelligence Platform

<p align="center">
  <strong>An End-to-End Data Analytics and Machine Learning Project for Monitoring AI Usage, Token Consumption, API Costs, Model Performance and Anomalies.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python" />
  <img src="https://img.shields.io/badge/SQL-PostgreSQL-336791?logo=postgresql" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Isolation%20Forest-orange" />
  <img src="https://img.shields.io/badge/Visualization-Power%20BI-yellow?logo=powerbi" />
  <img src="https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?logo=googlecolab" />
</p>

---

## 📌 Project Overview

**Token Analytics** is an AI Usage Monitoring and Cost Intelligence Platform designed to analyze Large Language Model (LLM) usage patterns, monitor token consumption, estimate API costs, evaluate model performance and identify unusual usage activities.

The project combines Python-based data analytics, PostgreSQL database management, machine learning-based anomaly detection and interactive Power BI dashboards to transform raw AI telemetry data into actionable business insights.

It helps organizations understand how AI resources are being consumed, identify expensive usage patterns, monitor system reliability and make data-driven decisions for optimizing AI operations.

## 🎯 Project Objectives

- Monitor AI/LLM API usage and interaction patterns.
- Analyze prompt, completion and total token consumption.
- Estimate AI API costs across different models and providers.
- Evaluate model response latency and quality.
- Analyze request failures and reliability indicators.
- Detect unusual usage patterns using Machine Learning.
- Build interactive Power BI dashboards.
- Generate business insights and optimization recommendations.

## 🏗️ System Architecture

```text
                 LLM TELEMETRY DATASET
                          |
                          v
                DATA COLLECTION
                  Python / Pandas
                          |
                          v
                DATA PREPROCESSING
             Cleaning and Transformation
                          |
                          v
              EXPLORATORY DATA ANALYSIS
              Statistical Analysis / EDA
                          |
                 +--------+--------+
                 |                 |
                 v                 v
          POSTGRESQL          MACHINE LEARNING
          SQL ANALYSIS        ISOLATION FOREST
                 |                 |
                 +--------+--------+
                          |
                          v
                 BUSINESS INSIGHTS
                          |
                          v
                  POWER BI DASHBOARD
                          |
                          v
                 ANALYTICAL REPORTS
```

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data processing and analytics |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical computations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine learning and anomaly detection |
| Isolation Forest | Unusual usage detection |
| PostgreSQL | Database storage and SQL analysis |
| SQLAlchemy | Python–PostgreSQL connectivity |
| Google Colab | Development environment |
| Power BI | Interactive business intelligence dashboards |
| Git & GitHub | Version control and project hosting |

## 📂 Dataset Information

**Dataset:** LLM System Ops Production Telemetry

**Source:** [Hugging Face – LLM System Ops Production Telemetry](https://huggingface.co/datasets/tarekmasryo/llm-system-ops-production-telemetry)

Dataset characteristics:

- Total records: 9,000
- Total columns: 55
- Format: CSV
- Data type: Synthetic telemetry data

### Important Dataset Attributes

| Category | Attributes |
|---|---|
| Interaction | interaction_id, session_id, user_id |
| Model Information | model_provider, model_name |
| Token Usage | prompt_tokens, completion_tokens, total_tokens |
| Cost Analysis | cost_usd |
| Performance | latency_ms, tokens_per_second |
| Quality | response_quality_score |
| Reliability | is_failure, failure_type |
| Safety | hallucination_flag, toxicity_flag |
| User Feedback | user_feedback_score, user_feedback_label |
| Anomaly Detection | anomaly_prediction, anomaly_score, anomaly_status |
| Time Analysis | timestamp_utc, hour_of_day_utc, day_of_week |

**Note:** The dataset contains synthetic telemetry records. Cost values represent dataset-provided estimates and should not be interpreted as actual provider invoices or live API billing.

## ⚙️ Project Implementation

### Phase 1 – Project Planning and Dataset Collection

- Defined the business problem and project objectives.
- Identified AI usage monitoring requirements.
- Selected the LLM System Ops Production Telemetry dataset.
- Loaded the CSV datasets into Google Colab.

### Phase 2 – Data Cleaning and Preprocessing

- Inspected dataset structure and data types.
- Handled missing user feedback values.
- Converted timestamp columns.
- Checked duplicate records.
- Validated token consumption values.
- Created additional analytical features.

### Phase 3 – Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand:

- Model-wise token consumption.
- Provider-wise estimated costs.
- Use-case distribution.
- Request trends over time.
- Latency distribution.
- Failure rates and failure types.
- Account-tier usage patterns.
- Response quality analysis.

### Phase 4 – PostgreSQL and SQL Analysis

- Configured PostgreSQL database using Neon.
- Connected Google Colab with PostgreSQL using SQLAlchemy.
- Created the `stg_interactions` table.
- Imported processed telemetry records.
- Created database indexes.
- Executed analytical SQL queries.

Key SQL analyses:

- Overall usage KPIs.
- Model-wise token consumption.
- Provider-wise cost analysis.
- Use-case cost analysis.
- Daily usage trends.
- Failure rate analysis.
- Latency analysis.
- Top token-consuming users.
- Expensive requests.
- Reliability analysis.

### Phase 5 – Machine Learning Anomaly Detection

Implemented the **Isolation Forest** algorithm using Scikit-learn to identify unusual AI usage patterns.

Features used include:

- Prompt tokens.
- Completion tokens.
- Total tokens.
- Estimated cost.
- Latency.
- Tokens per second.
- Tool calls.
- Retry index.
- Response quality.
- Time-based features.

The model identifies unusual interactions based on learned usage patterns.

**Model output:**
- Normal interactions.
- Anomalous interactions.
- Anomaly scores.
- Model-wise anomaly analysis.
- Use-case-wise anomaly analysis.

The anomaly detection contamination parameter was initially configured to 3%. This is a modelling assumption, not a verified real-world anomaly rate.

### Phase 6 – Power BI Dashboard Development

Developed an interactive Power BI dashboard to visualize AI usage and operational performance.

**Dashboard KPIs:**

- Total Requests
- Total Tokens
- Total Estimated Cost
- Average Latency
- Failure Rate
- Detected Anomalies

**Dashboard Visualizations:**

1. AI Requests Over Time
2. Anomaly Rate by Use Case
3. AI Model Cost vs Latency
4. Error Distribution
5. Top AI Models
6. AI Cost Trend
7. Usage by Country
8. Average Latency by Day

**Interactive filters:**
- Model Name
- Model Provider
- Date
- Month

### Phase 7 – Business Insights and Recommendations

Performed business-oriented analysis to identify:

- Models with the highest token consumption.
- Models with the highest estimated costs.
- Expensive AI use cases.
- Peak usage hours.
- Unusual usage patterns.
- Model performance and reliability trends.

Generated recommendations for cost optimization, token management, model selection, reliability monitoring and resource planning.

## 📊 Key Business Metrics

| Metric | Description |
|---|---|
| Total Requests | Total AI interactions analyzed |
| Total Tokens | Combined prompt and completion tokens |
| Estimated Cost | Dataset-estimated AI usage cost |
| Average Latency | Average response time in milliseconds |
| Failure Rate | Percentage of failed interactions |
| Anomaly Count | Number of interactions flagged as unusual |
| Cost per 1K Tokens | Estimated cost normalized by token volume |

## 📁 Repository Structure

```text
Token-Analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_sql_analysis.ipynb
│   └── 04_anomaly_detection.ipynb
│
├── reports/
│   ├── eda/
│   ├── sql/
│   ├── ml/
│   └── business_insights/
│
├── models/
│   └── isolation_forest_model.pkl
│
├── dashboard/
│   └── Token_Analytics.pbix
│
├── documentation/
│   └── Project_Report.pdf
│
├── requirements.txt
├── .gitignore
└── README.md
```

*This is the recommended repository structure. Include only folders and files that you have actually created.*

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/VijayReddy-07/Token-Analytics.git
```

```bash
cd Token-Analytics
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the Dataset

Download the dataset from:

[LLM System Ops Production Telemetry](https://huggingface.co/datasets/tarekmasryo/llm-system-ops-production-telemetry)

Place the downloaded CSV files inside:

```text
data/raw/
```

### 4. Run the Notebooks

Open the notebooks using Google Colab or Jupyter Notebook.

Execute them in the following order:

1. Data Preprocessing
2. Exploratory Data Analysis
3. SQL Analysis
4. Anomaly Detection

### 5. Configure PostgreSQL

Create a PostgreSQL database and configure the connection securely using environment variables.

Example:

```python
import os

DATABASE_URL = os.getenv("NEON_DATABASE_URL")
```

Never commit database passwords, API keys or connection credentials to GitHub.

### 6. Open the Power BI Dashboard

Open:

```text
Power BI Dashboard/Token analytics.jpeg
```

using Microsoft Power BI Desktop.

## 📦 Requirements

Example `requirements.txt`:

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
sqlalchemy
psycopg2-binary
joblib
pyarrow
```

## 🔮 Future Enhancements

- Real-time LLM API usage monitoring.
- Integration with live AI provider APIs.
- Automated cost alerts and budget monitoring.
- Advanced anomaly detection models.
- Predictive token consumption forecasting.
- Model recommendation based on cost and performance.
- Automated reporting and monitoring.
- Role-based access and multi-user monitoring.
## ⭐ Support

If you find this project interesting, consider giving the repository a ⭐ on GitHub.

---

<p align="center">
  <strong>Token Analytics – Turning AI Usage Data into Actionable Business Intelligence.</strong>
</p>
