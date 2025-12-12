
# Project_shodhAI — FinTech Loan Approval

---

## 📁 Files

```
EDA.ipynb     – Exploratory Data Analysis  
DL.ipynb      – Predictive / Deep Learning modeling  
RL.ipynb      – Offline RL loan-approval agent  
```

---

## ⚙️ Setup

### 1) Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate          # macOS/Linux
# venv\Scripts\activate           # Windows
```

### 2) Install Dependencies

Create a `requirements.txt`:

```
numpy
pandas
scikit-learn
joblib
notebook
jupyterlab
matplotlib
seaborn
gym     # optional (only for RL demos)
```

Install:

```bash
pip install -r requirements.txt
```
```
```


## 🧠 Offline RL Definition

**State:** Applicant feature vector
**Actions:**

* `0` → Deny
* `1` → Approve

**Reward Function:**

* Deny → `0`
* Approve + Fully Paid → `+ loan_amnt * int_rate`
* Approve + Default → `- loan_amnt`

---

## 🚀 Running the Project

### Step 1 — EDA

```bash
jupyter lab
```

Open **EDA.ipynb** → Run All.

### Step 2 — Train Offline RL Agent

Open **RL.ipynb** → Set `CSV_PATH` → Run All.
Models and policy files are automatically saved.

### Step 3 — Make Predictions

Use the exported policy wrapper to approve/deny new applicants.

---
