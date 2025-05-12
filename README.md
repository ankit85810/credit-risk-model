# Credit Risk Modeling App

This is a Streamlit-based web application [link](https://credit-risk-model-by-ankit.streamlit.app/) for predicting the **credit default risk** of a loan applicant using various financial and personal parameters. The app calculates the **default probability**, assigns a **credit score**, and categorizes the result into a **rating** (Poor, Average, Good, Excellent).

---

## 🚀 Features

- User-friendly web interface (built with Streamlit)
- Input fields for common credit parameters (income, loan amount, DPD, etc.)
- Real-time computation of:
  - Default probability
  - Credit score (scaled from 300 to 900)
  - Risk rating (Poor to Excellent)
- Model and preprocessing pipeline stored in a serialized `.joblib` file

---

## 🗂️ Project Structure

```
├── main.py                     # Streamlit app interface
├── prediction_helper.py       # Helper functions for data processing and prediction
├── requirements.txt           # Required Python packages
├── artifacts/
│   └── model_data.joblib      # Trained model, scaler, and metadata
```

---

## 📦 Setup Instructions

1. **Clone the repository**:

   ```bash
   git clone <https://github.com/ankit85810/credit-risk-model.git>
   cd credit-risk-model
   ```

2. **Create a virtual environment** (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the app**:

   ```bash
   streamlit run main.py
   ```

---

## 📈 How it Works

1. **User Input**: Provide inputs like age, income, loan amount, credit utilization, etc.
2. **Feature Engineering & Scaling**: Data is processed and scaled using a saved pipeline (`model_data.joblib`).
3. **Prediction**: A logistic regression model (or similar) predicts the default probability.
4. **Scoring**: Default risk is converted into a credit score and labeled into rating buckets.

---

## 🧠 Model Details

The `model_data.joblib` file contains:
- Trained classifier (`model`)
- Scaler used for normalization
- Feature names used in training
- Columns that require scaling

---

## ✅ Example Input

| Field                     | Example Value |
|--------------------------|---------------|
| Age                      | 28            |
| Income                   | 1,400,000     |
| Loan Amount              | 2,680,000     |
| Avg DPD                  | 25            |
| Credit Utilization Ratio | 30%           |
| Residence Type           | Owned         |
| Loan Purpose             | Education     |
| Loan Type                | Unsecured     |

---

## 📮 Contact

Created by **Ankit Vishwakarma** — MSc Data Science, NIT Rourkela  
For any questions, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/ankit-vishwakarma-500a7b324/).
