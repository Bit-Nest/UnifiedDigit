# Unified Prediction Flask Application

This repository contains a Flask-based web application that allows users to upload images and get predictions from two different machine learning models:

- **Decimal Prediction Model**: Recognizes decimal digits.
- **Devanagari Prediction Model**: Recognizes Devanagari characters.

The app acts as a unified interface to interact with these models, forwarding image uploads to the respective model backend services, receiving predictions, and displaying the results.

## Features

- Upload an image and get predictions from either the **Decimal** or **Devanagari** model.
- Provides both a web interface and API endpoints for ease of integration.
- Can be used as an API for programmatic access, such as with Postman or curl.
- Supports both **image file** and **model type** as inputs.

## Setup and Installation

### Prerequisites

- Python 3.x
- Flask
- Requests library

### 1. Clone the Repository

```bash
git clone https://github.com/Bit-Nest/UnifiedDigit.git
cd UnifiedDigit
```

2. Install Dependencies
Ensure you have the required Python packages installed by running:
```bash
pip install -r requirements.txt
```
3. Backend Models
The app forwards image requests to two separate API endpoints:

Decimal Model: Running on http://localhost:5100
Devanagari Model: Running on http://localhost:5200

Make sure you have the backend services running on these respective ports before starting the Flask app.

4. Start the Flask Application
To run the Flask application:
```bash
python app.py
```
By default, the app will be hosted at http://localhost:5300.

6. Testing the API
You can use an API client like Postman or curl to test the predictions.

Example Request (POST)
Endpoint: http://localhost:5300/predict

Parameters:
```bash
image (form-data): The image file to be analyzed.
model_type (form-data): Either decimal or devanagari.
```
