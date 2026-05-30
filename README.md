# 🛡️ ML-Powered Intrusion Detection & Honeypot System

A real-time **network intrusion detection system** combining machine learning with a honeypot module to detect, monitor, and log cyber attacks. Built with Python, Flask, and Scikit-learn using the NSL-KDD benchmark dataset.

---

## 🚀 Features

- **Real-time attack detection** across multiple attack categories (DoS, Probe, R2L, U2R)
- **Honeypot module** to simulate vulnerable services and capture attacker behavior
- **Flask dashboard** to visualize live network traffic, anomalies, and model metrics
- **ML pipeline** with feature scaling, label encoding, and multi-class classification
- Evaluated with precision, recall, and F1-score metrics

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | Python 3.x |
| Web Framework | Flask |
| ML Library | Scikit-learn |
| Dataset | NSL-KDD |
| Frontend | HTML, CSS, JavaScript |
| Visualization | Matplotlib / Plotly |

---

## 📁 Project Structure

```
intrusion-detection-honeypot/
│
├── app.py                  # Flask app entry point
├── model/
│   ├── train.py            # Model training script
│   ├── predict.py          # Real-time prediction logic
│   └── model.pkl           # Saved trained model
│
├── honeypot/
│   └── honeypot.py         # Honeypot simulation module
│
├── data/
│   └── NSL_KDD_Train.csv   # Training dataset
│
├── templates/
│   └── dashboard.html      # Monitoring dashboard UI
│
├── static/
│   └── style.css
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/intrusion-detection-honeypot.git
cd intrusion-detection-honeypot

# 2. Create a virtual environment
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Train the model
python model/train.py

# 5. Run the Flask app
python app.py
```

Then open your browser at `http://localhost:5000`

---

## 🧠 ML Model Details

- **Dataset:** NSL-KDD (improved version of KDD Cup 99)
- **Preprocessing:** Label encoding for categorical features, StandardScaler for normalization
- **Algorithm:** Random Forest Classifier (+ experiments with Decision Tree, SVM)
- **Classes:** Normal, DoS, Probe, R2L, U2R
- **Evaluation Metrics:** Precision, Recall, F1-Score, Confusion Matrix

---

## 🕵️ Honeypot Module

The honeypot simulates common vulnerable services to attract and log attacker activity:
- Captures IP addresses, timestamps, and attack patterns
- Logs are stored and visualized on the Flask dashboard
- Helps in understanding attacker behavior and threat intelligence

---

## 📊 Dashboard Preview

The Flask-based monitoring dashboard displays:
- Live network traffic feed
- Flagged anomalies with attack type classification
- Model performance metrics (accuracy, F1-score)
- Honeypot activity logs

---

## 📦 Requirements

```
flask
scikit-learn
pandas
numpy
matplotlib
plotly
```

---

## 🙋‍♂️ Author

**Shravan Sharma**  
B.E. Computer Engineering — Sinhgad Institute of Technology, Lonavala  
📧 shravancsharma19@gmail.com  
📍 Pune, Maharashtra

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
