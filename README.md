# **TuneScope: Big Data Analytics on Spotify**

> **A Big Data Analytics Capstone Project**
> *School of Management Studies, University of Hyderabad*
> *Course: Big Data Analytics*
> **By:** Boddapati Kanchana (Roll No: 24MBMB02)
> **Faculty Guide:** Sree Lakshmi Mam

---

## **Project Overview**

**TuneScope** is a Big Data Analytics project that explores large-scale Spotify and lyrics datasets to uncover **patterns in song popularity, lyrical sentiment, artist performance, and genre behavior**.
The project integrates **PySpark**, **Databricks**, and **machine learning models** to analyze both audio and textual data, visualized through an interactive **Databricks Dashboard** called **TuneScope 2.0**.

This repository contains all source code, data pipeline notebooks, model files, and the final presentation with voice narration.

---

## **Objectives**

* To build a **scalable Big Data pipeline** using Databricks and PySpark.
* To integrate **audio and lyrical data** for multi-dimensional analysis.
* To implement **machine learning models** predicting song popularity and clustering songs by similarity.
* To apply **sentiment analysis (NLP)** on song lyrics.
* To visualize analytical insights through an **interactive dashboard**.

---

## **Project Architecture**

The project follows a **Bronze–Silver–Gold data pipeline** architecture, enabling efficient and modular data processing:

| Layer            | Function                                        | Output Tables                                                                                                          |
| ---------------- | ----------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Bronze Layer** | Raw data ingestion (Spotify & Lyrics datasets)  | `bronze_spotify`, `bronze_lyrics`                                                                                      |
| **Silver Layer** | Data cleaning, transformation, merging          | `silver_songs`                                                                                                         |
| **Gold Layer**   | Feature engineering, ML modeling, and analytics | `gold_sentiment`, `gold_genre_profile`, `gold_artist_performance`, `gold_popularity_features`, `gold_cluster_features` |

---

## **Technologies & Tools Used**

| Category            | Technology / Tool                   | Purpose                              |
| ------------------- | ----------------------------------- | ------------------------------------ |
| **Platform**        | Databricks (Community Edition)      | Unified environment for PySpark & ML |
| **Programming**     | Python, PySpark                     | Big data processing and analysis     |
| **Libraries**       | Spark MLlib, scikit-learn, TextBlob | Regression, Clustering, and NLP      |
| **Storage**         | Delta Tables (Databricks Catalog)   | Persistent data layers               |
| **Visualization**   | Databricks Dashboard                | Interactive visual analytics         |
| **Version Control** | GitHub                              | Code and document repository         |

---

## **Use Cases Implemented**

| No.   | Use Case                     | Method                            | Visualization  | Key Insight                                   |
| ----- | ---------------------------- | --------------------------------- | -------------- | --------------------------------------------- |
| **1** | Song Popularity Prediction   | Linear Regression (PySpark MLlib) | Bar Chart      | Danceability & Valence drive song popularity  |
| **2** | Sentiment Analysis of Lyrics | TextBlob NLP                      | Pie Chart      | Positive sentiment dominates mainstream music |
| **3** | Genre Profiling              | Aggregation by genre              | Bar Chart      | EDM & Dance genres show highest energy        |
| **4** | Artist Performance Analysis  | Statistical aggregation           | Horizontal Bar | Artist popularity correlates with diversity   |
| **5** | Song Clustering              | MiniBatch KMeans (scikit-learn)   | Scatter Plot   | Songs form natural mood-based clusters        |

---

## **Dashboard Overview**

**Dashboard Name:** TuneScope: Big Data Analytics on Spotify
**Platform:** Databricks Visualization Interface

The dashboard consolidates all five use cases into an interactive visual format with:

* Bar charts for regression coefficients and genre profiling
* Pie chart for sentiment analysis
* Horizontal bar for artist popularity
* Scatter plot for clustering results

*Refer to:* `Dashboard.html` (exported from Databricks)

---

## **Repository Structure**

```
TuneScope_Project/
│
├── 01_ingest_bronze.py           # Data ingestion (Bronze layer)
├── 02_clean_silver.py            # Data cleaning and merging (Silver layer)
├── 03_feature_engineering.py     # Feature engineering and sentiment scoring (Gold layer)
├── 04_models_and_usecases.py     # ML models and analytical use cases
├── 05_visualisations.py          # Dashboard visualizations
├── master_pipeline_runner.py     # Pipeline orchestration script
│
├── spotify_songs.csv             # Spotify dataset
├── lyrics_10k.csv                # Lyrics dataset
│
├── Dashboard.html                # Interactive dashboard export
├── Code.ipynb                    # Combined notebook version (for reference)
├── TuneScope_Presentation.pptx   # Final presentation with voice-over
│
└── README.md                     # Project documentation
```

---


## **Limitations**

* Databricks CE memory limitations (2 GB).
* Dataset restricted to 10,000 songs.
* Lexicon-based sentiment (TextBlob) lacks deep contextual analysis.
* No real-time streaming integration.

---

## **Future Enhancements**

* Integrate **real-time streaming** using Apache Kafka + Spark Streaming.
* Replace TextBlob with **Transformer-based NLP models (BERT, RoBERTa)**.
* Build **automated recommendation systems** using cluster-based filtering.
* Extend dashboard to **Power BI / Tableau** for richer user experience.
* Deploy pipeline on **Databricks (AWS/Azure)** for large-scale analytics.

---

## **Conclusion**

The *TuneScope* project successfully demonstrates how **Big Data Analytics** can be applied to the **media and entertainment industry** to derive meaningful insights from music data.
By combining **audio and lyrical features**, the system reveals patterns in popularity, sentiment, and genre behavior.
The integration of PySpark, Databricks, and NLP techniques creates a scalable analytical workflow capable of supporting **data-driven creativity and personalization** in music streaming platforms.

---

##  **Acknowledgements**

I extend my heartfelt gratitude to **Sree Lakshmi Mam**, faculty guide, for her continuous guidance and mentorship throughout this project.
Special thanks to the **School of Management Studies, University of Hyderabad**, for providing the infrastructure and academic support.
I also thank my peers and classmates for their valuable feedback and encouragement.

---

