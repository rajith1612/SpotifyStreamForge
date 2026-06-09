# 🎵 SpotifyStreamForge — Real-Time Music Streaming Data Engineering Pipeline

> Built by **Lakshman Rajith Rongala** | University of New Haven | [LinkedIn](https://www.linkedin.com/in/lakshmanrajith) | [Portfolio](https://heartfelt-zabaione-89c939.netlify.app) | [GitHub](https://github.com/rajith1612)

![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)
![Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

---

## 🚀 Overview

**SpotifyStreamForge** is a production-grade, end-to-end real-time data engineering pipeline that ingests live music streaming events (user plays, skips, searches, and authentications) via **Apache Kafka**, processes them in real-time with **Apache Spark Streaming**, transforms using **dbt**, orchestrates with **Apache Airflow**, and delivers analytics-ready dashboards on **Google BigQuery**.

Built to answer business-critical questions like:
- 🎧 What are the most played songs right now?
- 👥 Who are the most active users and when?
- 🌍 What genres are trending by region?
- 📈 How does listening behavior change over time?

---

## 🏗️ Architecture

```
Eventsim (Music Events)
        ↓
Apache Kafka (Streaming Ingestion)
        ↓
Apache Spark Streaming (Real-Time Processing)
        ↓
Google Cloud Storage (Data Lake)
        ↓
Apache Airflow (Hourly Batch Orchestration)
        ↓
Google BigQuery (Data Warehouse)
        ↓
dbt (Transformations & Data Modeling)
        ↓
Looker Studio / Power BI (Dashboard)
```

---

## ✨ Features

- 🔄 **Real-Time Streaming** — Kafka ingests 1M+ user events per day
- ⚡ **Spark Streaming** — Processes events every 2 minutes into GCS data lake
- 🔧 **dbt Transformations** — Builds star schema models with tests and documentation
- 📅 **Airflow Orchestration** — Hourly DAGs trigger batch processing and warehouse loads
- ☁️ **GCP Infrastructure** — Terraform-provisioned Kafka, Spark, and Airflow VMs
- 📊 **Analytics Dashboards** — Tracks top songs, active users, and listening trends

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Streaming | Apache Kafka, Zookeeper |
| Processing | Apache Spark Streaming, PySpark |
| Orchestration | Apache Airflow |
| Transformation | dbt (models, tests, documentation) |
| Data Lake | Google Cloud Storage (GCS) |
| Data Warehouse | Google BigQuery |
| Infrastructure | Terraform, GCP Compute Engine |
| Containerization | Docker, Docker Compose |
| Language | Python, SQL |

---

## 📁 Project Structure

```
SpotifyStreamForge/
├── airflow/                  # Airflow DAGs and configs
├── dbt/                      # dbt models, tests, documentation
│   ├── models/
│   │   ├── staging/          # Raw to staging transformations
│   │   └── core/             # Fact and dimension tables
├── kafka/                    # Kafka producer and consumer
├── spark_streaming/          # PySpark streaming jobs
├── terraform/                # Infrastructure as Code
├── scripts/                  # VM setup and utility scripts
├── images/                   # Architecture diagrams
└── README.md
```

---

## 📊 Dashboard Preview

The analytics dashboard tracks:
- **Top Songs** — Most played tracks in real-time
- **Active Users** — User activity by hour and location
- **Genre Trends** — Trending genres by region
- **Artist Popularity** — Most listened artists by play count

---

## 📈 Key Results

| Metric | Result |
|--------|--------|
| Events Processed | 1M+ daily |
| Streaming Latency | ~2 minutes |
| Batch Processing | Hourly via Airflow |
| dbt Models | 10+ staging + core models |
| Dashboard KPIs | Top songs, users, genres, artists |

---

## ⚙️ Setup & Usage

```bash
# Clone the repo
git clone https://github.com/rajith1612/SpotifyStreamForge.git
cd SpotifyStreamForge

# Provision GCP infrastructure
cd terraform
terraform init
terraform apply

# Start Kafka
cd kafka
docker-compose up

# Start Spark Streaming
spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.1.2 stream_all_events.py

# Start Airflow
cd airflow
docker-compose up

# Run dbt transformations
cd dbt
dbt run
dbt test
```

---

## 📬 Contact

**Lakshman Rajith Rongala**
- 📧 Email: lakshmanrajith777@gmail.com
- 💼 LinkedIn: [linkedin.com/in/lakshmanrajith](https://www.linkedin.com/in/lakshmanrajith)
- 🌐 Portfolio: [heartfelt-zabaione-89c939.netlify.app](https://heartfelt-zabaione-89c939.netlify.app)
- 🐙 GitHub: [github.com/rajith1612](https://github.com/rajith1612)
