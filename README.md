# SummerAnalyticsCapstoneProject

# 🚗 Dynamic Pricing for Urban Parking Lots

**Capstone Project - Summer Analytics 2025**  
hosted by the Consulting & Analytics Club × Pathway

---

## 📌 Project Overview

Urban parking spaces in crowded cities face issues of under-utilization or overcrowding due to static pricing policies. To address this, our project develops an **intelligent dynamic pricing engine** that updates parking fees in real time based on factors like demand, queue length, traffic congestion, special events, vehicle type, and competitor prices.  

The project supports **14 parking lots** and uses historical + live streaming data to optimize pricing strategies. Three progressively sophisticated models were developed:  

- **Model 1 (Baseline Linear)**: price based on current occupancy  
- **Model 2 (Demand-Based)**: considers occupancy, queue, traffic, special days, and vehicle type  
- **Model 3 (Competitive)**: adds competitor pricing and geographic proximity

Pricing updates are visualized in real time using Bokeh, streamed using Pathway-like simulated pipelines, and built fully from scratch with only pandas, numpy, and Pathway.

---

## 🛠 Tech Stack

- **Python 3.10**
- **Google Colab** (Jupyter-compatible)
- **Pandas, NumPy** (core data processing)
- **Pathway** (for stream simulation)
- **Bokeh** (visualization)
- **Mermaid** (for architecture diagrams)
- **GitHub** (version control)

---

## 📊 Project Architecture

```mermaid
graph TD
    A[CSV Data Source] --> B[Pathway Data Stream]
    B --> C[Data Preprocessing & Feature Engineering]
    C --> D[Model 1: Linear Pricing]
    C --> E[Model 2: Demand-Based Pricing]
    C --> F[Model 3: Competitive Pricing]
    D --> G[Pricing Output]
    E --> G
    F --> G
    G --> H[Bokeh Visualization]
    G --> I[Rerouting Suggestions]
