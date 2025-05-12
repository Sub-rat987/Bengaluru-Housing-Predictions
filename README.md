## Bengaluru Housing Price Prediction

This project is a complete end-to-end machine learning application that predicts real estate prices in Bengaluru, India. It involves data preprocessing, model training with `scikit-learn`, and serving the model through a Flask-based web interface. The goal is to provide a simple and interactive frontend where users can input property features and get estimated prices instantly.

---

### Tech Stack

- **Language**: Python 3.13+
- **Framework**: Flask (for API and web server)
- **ML Libraries**: scikit-learn, pandas, numpy
- **Frontend**: HTML, CSS, JavaScript (Vanilla)
- **Deployment**: Tested on Render

---

### Project Structure

```
Bengaluru-Housing-Predictions/
│
├── client/
│   ├── app.js              # Handles frontend logic and fetch API calls
│   ├── index.html          # Webpage layout for input and result display
│   └── style.css           # Basic styling for the UI
│
├── model/
│   ├── bengaluru_home_prices.csv  # Dataset used for training
│   ├── home_price_model.pickle    # Trained Linear Regression model
│   └── columns.json               # Stores model input feature names
│
├── server/
│   └── server.py          # Main Flask application that serves the model
│
├── requirements.txt       # Python dependencies with pinned versions
└── README.md              # Project overview and instructions
```

---

### Setup Instructions

1. **Clone the Repository**

```bash
git clone https://github.com/Sub-rat987/Bengaluru-Housing-Predictions.git
cd Bengaluru-Housing-Predictions
```

2. **Set Up a Virtual Environment**

```bash
python3 -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```

3. **Install Python Dependencies**

```bash
pip install -r requirements.txt
```

4. **Run the Flask Server**

```bash
python3 server/server.py
```

5. **Access the Web Application**

Open a browser and go to:  
`http://127.0.0.1:10000` or the local IP listed in terminal

---

### How It Works

1. **Preprocessing**: The model uses location and size-related features to predict property price.
2. **Model**: A Linear Regression model is trained and serialized (`home_price_model.pickle`).
3. **Serving**: Flask exposes API endpoints that accept JSON inputs and return predictions.
4. **Frontend**: JavaScript captures user input and calls the backend API to fetch predictions dynamically.

---

### Notes

- The current setup is intended for local development. For production use, deploy via a WSGI server such as Gunicorn or on platforms like Render.
- The model was trained using `scikit-learn==1.5.1`. Ensure compatibility when loading the model in newer environments.

