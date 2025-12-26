# tehran_houses
Synthetic Tehran housing dataset with geolocation extraction for spatial analysis and price prediction using machine learning.
🏠 Tehran Housing Geolocation & Data Analysis Project
📌 Project Overview

This project aims to collect geographical coordinates (latitude & longitude) of residential properties in Tehran and analyze housing prices based on physical and spatial features.

A large-scale synthetic yet realistic dataset of Tehran housing data is used to support:

Machine Learning models

Data analysis and visualization

Price prediction systems

GIS and spatial analysis

📊 Dataset Description

The dataset contains over 200,000 residential property records across Tehran neighborhoods.

Dataset Features:
Column	Description
neighborhood	Neighborhood name
area	Property area in square meters (40–300)
rooms	Number of rooms (1–5)
age	Building age (0–25 years)
parking	Parking availability (0 = No, 1 = Yes)
price	Property price (Toman – algorithmically estimated)

📁 Dataset file:

tehran_housing_synthetic_all_neighborhoods.csv

🌍 Geolocation Extraction

For each property, geographical coordinates are obtained based on its neighborhood.

Workflow:

Read neighborhood names from the dataset

Use a geocoding API (e.g., Nominatim / OpenStreetMap or Google Maps API)

Append the following columns:

latitude

longitude

These coordinates enable:

Spatial price analysis

Map visualization

Location-aware machine learning models

⚙️ Project Pipeline

Load the CSV dataset

Data cleaning and preprocessing

Fetch neighborhood coordinates via geocoding APIs

Merge spatial and numerical features

Perform analysis or train price prediction models

🧠 Use Cases

Housing price prediction in Tehran

Analyzing the impact of location on property prices

Academic AI / Data Science projects

GIS-based spatial modeling

🛠 Technologies Used

Python

Pandas

NumPy

Geopy / Requests

Jupyter Notebook

👨‍🎓 Educational Purpose

This project is designed as a university-level practical assignment, focusing on:

Working with large-scale datasets

API-based data collection

Data preprocessing for AI models

Spatial data analysis

⚠️ Disclaimer

The dataset is synthetic and not real market data, but it is generated based on realistic housing market patterns in Tehran and is intended solely for educational and research purposes.
