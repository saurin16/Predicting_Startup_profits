# Startup Profits Prediction System and Flask API Deployment

## Overview

This system predicts profits for startup companies based on various factors such as R&D spending, administration expenses, marketing expenses, and the state in which the startup is located. Additionally, it includes a Flask API deployment, allowing users to interact with the prediction model via API requests.
![Poject](image.png)

## Exploratory Data Analysis

### Data Description

The dataset contains information from 50 startup companies located in New York, California, and Florida. The variables in the dataset are:

- **R&D Spend**: Research and Development Expenses
- **Administration**: Administration Costs
- **Marketing Spend**: Marketing Expenses
- **State**: Location of the Startup
- **Profit**: Profit Generated by the Startup

[//]: # "Include your EDA steps and findings here."

## Feature Engineering and Model Building

[//]: # "Include your feature engineering steps, model selection, and training details here."

## Flask API Deployment

### Usage

#### Prediction Endpoint

- **URL**: `https://your-app-url/predict`
- **Method**: POST
- **Request Body**: JSON object with the following fields:
  - `R&D Spend`: float, Research and Development Expenses
  - `Administration`: float, Administration Costs
  - `Marketing Spend`: float, Marketing Expenses
  - `State`: string, Location of the Startup (New York, California, or Florida)

**Example Request:**

```json
{
  "R&D Spend": 100000,
  "Administration": 120000,
  "Marketing Spend": 200000,
  "State": "New York"
}
```

**Example Response:**

```json
{
  "prediction": 125000.0
}
```

#### Health Check Endpoint

- **URL**: `https://your-app-url/health`
- **Method**: GET
- **Response**: `"Healthy"`

Use this endpoint to check if the Flask API service is running properly.

### Deployment

This Flask API service is deployed on Heroku.

## Development

### Installation

To set up the development environment, follow these steps:

1. Clone this repository.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the Flask API service locally:

   ```bash
   flask run
   ```

### Testing

To run tests, use the following command:

```bash
pytest
```

## Credits

This Flask API service is based on the startup profits prediction model trained by SAURIN.
