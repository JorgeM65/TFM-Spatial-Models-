# TFM - Spatial Prediction with GWR and GW-SVR

This repository contains the full code developed for the Master's Thesis in Big Data Analytics, focused on analyzing and comparing the performance of global and geographically weighted regression models for spatial prediction tasks.

## 📌 Project Objective

The aim of this project is to evaluate the predictive behavior of:
- **Linear Regression (LR)**
- **Support Vector Regression (SVR)**
- **Geographically Weighted Regression (GWR)**
- **Geographically Weighted Support Vector Regression (GW-SVR)**

The random split stability of these models are tested across several benchmark datasets (Georgia, Columbus, PM2.5, Baltimore, and a synthetic dataset), and finally applied to a real-world case study: predicting the number of Airbnb listings in the city of Barcelona at the census-section level.

## 🗂️ Repository Structure

├── Airbnb/ # Contains the Airbnb case study

│ ├── Airbnb_def.ipynb # Notebook for generating results in the Case Study section

│ ├── sections_2017.csv # Dataset with Airbnb data

│ └── sections_geo.json # GeoJSON file with geographic information of Barcelona

├── Stability/ # Contains the stability analysis for benchmark datasets

│ ├── Data/ # Raw datasets (Georgia, Columbus, Baltimore, etc.)

│ ├── Results/ # Output results for each dataset

│ ├── Baltimore_loop.ipynb # Code for the Baltimore dataset

│ ├── Columbus_loop.ipynb # Code for the Columbus dataset

│ ├── Georgia_loop.ipynb # Code for the Georgia dataset

│ ├── Pm25_loop.ipynb # Code for the PM2.5 dataset

│ ├── Sintetico_loop.ipynb # Code for the synthetic dataset

│ └── Tables.ipynb # Code for generating metrics tables and plots

├── requirements.txt # Python libraries and versions used

└── README.md # This file

## 🧪 Main Components

- **Model Implementation:** Custom implementation of GWR and GW-SVR.
- **Kernel Functions:** Including classical Gaussian kernel and a novel Gaussian+KNN hybrid kernel.
- **Bandwidth Selection:** LOOCV-based and adapted strategies for each model.
- **Performance Metrics:** MAE, RMSE, NMSE, MAPE and REP for comparison.
- **Stability Analysis:** Evaluation across different train/test seeds.
- **Real Case Study:** Barcelona Airbnb listings prediction using geospatial features.

## 📊 Results Overview

GWR consistently outperformed global models in heterogeneous spatial settings. The GW-SVR model showed additional improvements in synthetic and complex real-world data when using an adaptive hybrid kernel.

## 🛠️ Installation

It is recommended to use a virtual environment (e.g. `venv` or `conda`):

## 📄 License
This project is released under the MIT License. Feel free to use and cite appropriately.

## 👤 Author
Jorge Manrique Ruiz

Master in Big Data Analytics

Universidad Carlos III de Madrid (UC3M), 2025


