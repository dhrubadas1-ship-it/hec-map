Human-Elephant Conflict (HEC) Prediction Dashboard

This project provides an interactive dashboard to visualize predicted human-elephant conflict (HEC) zones in Sonitpur, Assam. It combines machine learning predictions with geospatial visualization and feedback collection.

Key Features

ML-Based Predictions

A Random Forest Classifier is trained on historical HEC data to identify high-risk grid cells.

The model considers factors like elephant counts, crop damage, human injury, and previous conflict records.

Predictions are saved as a CSV (hec_grid_predicted_high_prob_YYYY-MM-DD.csv), which the dashboard uses to display markers.

Interactive Map

Displays predicted HEC zones with markers.

Marker size or color reflects the predicted probability or number of elephants.

Prediction Table

A table lists each grid cell with latitude, longitude, predicted elephant count, and probability.

Each row includes a prefilled Google Form link for local feedback collection.

Feedback Integration

Local users can submit observed counts or confirm predictions through prefilled forms.

Helps improve model accuracy over time by collecting real-world observations.

GitHub Pages Deployment

The dashboard is live on GitHub Pages (https://dhrubadas1-ship-it.github.io/hec-map/).

Easy to update with new predictions.

Project Workflow

Model Training

hec_model_with_behavior.py trains the ML model offline using historical data.

The model outputs predicted probabilities for each grid cell.

CSV Generation

Predicted high-probability HEC zones are exported to a CSV.

Dashboard Generation

generate_hec_dashboard_final.py reads the CSV and generates index.html.

The HTML contains the map, table, and prefilled feedback links.

Can be tested locally and pushed to GitHub Pages for live access.

Why ML

Using a machine learning model allows data-driven predictions instead of relying solely on rules or manual thresholds.

The model can learn complex patterns from historical HEC incidents to identify areas at risk.