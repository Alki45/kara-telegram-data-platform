# Kara Telegram Data Platform

This project implements an end-to-end data platform that extracts, transforms, enriches, and exposes insights from public Telegram channels related to Ethiopian medical businesses.

Developed as part of the 10 Academy Artificial Intelligence Mastery program, the platform integrates modern data engineering tools including Telethon, dbt, YOLOv8, FastAPI, and Dagster.

---

## 🚀 Overview

**Business Goal:**  
Help stakeholders in Ethiopia's health sector identify trends, products, pricing, and activity patterns from Telegram channels by delivering a scalable, maintainable, and insightful data product.

---

## 🧱 Project Architecture

**Tools & Technologies:**
- **Data Extraction**: [Telethon](https://docs.telethon.dev/en/stable/) (Telegram scraping)
- **Data Transformation**: [dbt](https://www.getdbt.com/) with PostgreSQL (staging and star schema)
- **Data Enrichment**: [YOLOv8](https://docs.ultralytics.com/) for object detection in images
- **API Layer**: [FastAPI](https://fastapi.tiangolo.com/) for exposing analytical insights
- **Orchestration**: [Dagster](https://dagster.io/) for pipeline automation
- **Environment Management**: Docker + `.env` for secrets

---

## 📊 Business Questions Answered

- What are the **top 10 most frequently mentioned** medical products?
- How does the **price or availability** of a product vary across channels?
- Which channels have the **most visual content** (images of pills, creams, etc.)?
- What are the **daily and weekly posting trends** for medical topics?

---

## 📁 Project Structure

```bash
kara-telegram-data-platform/
├── .env                      # Secrets and credentials
├── .gitignore                # Git ignore rules
├── README.md                 # This file
├── docker-compose.yml        # Docker configuration
├── Dockerfile                # Python app container
├── requirements.txt          # Python dependencies
├── data/
│   └── raw/telegram_messages/YYYY-MM-DD/
├── dbt_project/
│   ├── models/staging/
│   ├── models/marts/
│   └── dbt_project.yml
├── scraping/
│   └── telegram_scraper.py
├── enrichment/
│   └── yolo_enrichment.py
├── api/
│   ├── main.py
│   ├── database.py
│   ├── schemas.py
│   └── crud.py
├── orchestration/
│   ├── pipeline.py
│   └── dagster_pipeline.py
└── diagrams/
    ├── architecture.png
    └── star_schema.png
