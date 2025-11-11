# 🏦 Bank Customer Churn Prediction with ANN

This project predicts **customer churn** (whether a customer will leave the bank) using an **Artificial Neural Network (ANN)** built with **TensorFlow** and deployed using **Streamlit**.

---

## 🚀 Project Overview

Customer churn prediction is crucial for banks to identify customers likely to leave and take proactive retention actions.  
This project uses customer demographic, financial, and behavioral data to predict churn probability.

---

## 🧠 Model Details

- **Framework:** TensorFlow / Keras  
- **Model Type:** Artificial Neural Network (ANN)  
- **Encoders Used:**  
  - `LabelEncoder` for gender  
  - `OneHotEncoder` for geography  
- **Feature Scaling:** `StandardScaler`  
- **Saved Files:**  
  - `model.h5` — Trained ANN model  
  - `label_encoder_gender.pkl` — Encodes Gender feature  
  - `onehot_encoder_geo.pkl` — Encodes Geography feature  
  - `scaler.pkl` — StandardScaler object  

---

## 🧾 Input Features

| Feature | Description | Example |
|----------|--------------|----------|
| Geography | Country of the customer | France, Germany, Spain |
| Gender | Male / Female | Male |
| Age | Customer age | 35 |
| Credit Score | Customer's creditworthiness | 600 |
| Balance | Account balance | 50000 |
| Estimated Salary | Salary estimate | 70000 |
| Tenure | Number of years with the bank | 5 |
| NumOfProducts | Number of products used | 2 |
| HasCrCard | Whether customer has a credit card | 1 |
| IsActiveMember | Whether customer is active | 0 |

---

## 🧩 How It Works

1. User enters input values in the Streamlit interface.
2. Encoders transform categorical variables (Gender, Geography).
3. Features are scaled using the saved `StandardScaler`.
4. The ANN model (`model.h5`) predicts churn probability.
5. Output:
   - **Churn Probability** (0–1)
   - **Prediction Message** (“Likely to churn” or “Not likely to churn”)

---

## 💻 How to Run Locally

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/bank-customer-churn-prediction.git
cd bank-customer-churn-prediction
```


2️⃣ Create Virtual Environment
```bash
python -m venv venv
venv\Scripts\activate  # On Windows
source venv/bin/activate  # On macOS/Linux
```

3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

4️⃣ Run the App
```bash
streamlit run app.py
```

📦 Project Structure
```bash
📁 Bank Customer Churn Prediction
│
├── app.py                        # Streamlit web app
├── model.h5                      # Trained ANN model
├── label_encoder_gender.pkl      # LabelEncoder for Gender
├── onehot_encoder_geo.pkl        # OneHotEncoder for Geography
├── scaler.pkl                    # StandardScaler for features
├── requirements.txt              # Required Python libraries
└── README.md                     # Project documentation

```

🧮 Example Output
```bash
Churn Probability: 0.78
The customer is likely to churn.
```

🧑‍💻 Author

Dhruv Parmar
📧 dhruvparmar70441@gmail.com