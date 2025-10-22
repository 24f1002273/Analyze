# Product Performance Dashboard

This repository contains a complete, functional single-page web application (`index.html`) that visualizes aggregated product category performance data. The data is processed by a Python script (`execute.py`), stored in a CSV file (`data.csv`), and generated via a GitHub Actions CI/CD pipeline. The final processed data (`result.json`) is then published to GitHub Pages, which the frontend application fetches and displays.

## Project Summary

The project consists of three main components:

1.  **Backend Logic (`execute.py`):** A Python script that reads product data, calculates key financial metrics (Revenue, Cost, Profit, Profit Margin), aggregates this data by product category, and outputs the result in JSON format. This script has been fixed to resolve a non-trivial error (`pd.data_frame` typo, and 'revenew' misspellings).
2.  **Data Source (`data.csv`):** A comma-separated values file derived from `data.xlsx`, serving as the input for the Python script.
3.  **CI/CD Pipeline (`.github/workflows/ci.yml`):** A GitHub Actions workflow that automates the process of linting the Python code with Ruff, executing the Python script, and publishing the generated `result.json` file to GitHub Pages.
4.  **Frontend Application (`index.html`):** A single-page web application (HTML, CSS, JavaScript) that fetches the `result.json` from GitHub Pages and presents the data in an interactive, professional-looking table using Bootstrap.

## Setup Instructions

To set up this project locally or understand its structure for deployment:

### 1. Clone the Repository