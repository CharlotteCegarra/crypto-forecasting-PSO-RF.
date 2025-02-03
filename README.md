
# PSO RF - Predicting Cryptocurrency Returns and Optimizing Portfolios

## 📖 Project Overview
This project is part of the **Quantitative Finance course** within the Master MOSEF (Modélisation et Méthodes Mathématiques en Économie et Finance) at **Paris 1 Panthéon-Sorbonne University**. The goal is to **forecast cryptocurrency returns** and **optimize portfolio allocations** using advanced machine learning methods.

### Key Objectives:
1. **Accurate Return Forecasting**:
   - Use a **Random Forest model** optimized with **PSO (Particle Swarm Optimization)** to predict cryptocurrency returns.
   - Leverage historical market data and technical indicators to inform predictions.

2. **Portfolio Optimization**:
   - Apply **Mean-Variance Forecasting (MVF)** to dynamically allocate assets based on predicted returns.
   - Compare portfolio performance against benchmark strategies using metrics such as the Sharpe ratio.

This project combines **machine learning**, **portfolio theory**, and **cryptocurrency analytics** to provide a comprehensive framework for research in quantitative finance.

---

## 👩‍💻 Authors
- **Hella Bouhadda**
- **Charlotte Cegarra**
- **Chirine Doxposito**

---

## 📂 Project Structure
```bash
📦 crypto-forecasting-PSO-CNN
│
├── 📂 crypto_api/                  # Core of the API
│   ├── 📂 data/                    # Data storage
│   │   ├── 📂 processed/           # Processed and cleaned data
│   │   │   ├── `features_data.csv` 
│   │   │   ├── `merged_data.csv`
│   │   ├── 📂 raw/                 # Raw scraped data
│   │       ├── `Bitcoin_(BTC)_yahoo_data.csv`
│   │       ├── `Ethereum_(ETH)_yahoo_data.csv`
│   │       ├── `...` (Other cryptocurrencies)
│   ├── 📂 data_processing/         # Data processing scripts
│   │   ├── `features.py`           # Feature engineering
│   │   ├── `scrape.py`             # Web scraping for raw data
│   ├── 📂 ml/                      # Machine learning scripts
│   │   ├── `mvf.py`                # Portfolio optimization using MVF
│   │   ├── `predict.py`            # Prediction logic for market direction
│   │   ├── `train.py`              # Model training scripts
│   ├── 📂 static/                  # Static files for API documentation
│   │   ├── `logo.jpg`             
│   ├── 📂 templates/               # HTML templates
│   │   ├── `home.html`             # API home page
│   ├── `API_README.md`             # API documentation
│   ├── `config.py`                 # Configuration file for paths and settings
│   ├── `direction_model.pkl`       # Pre-trained market direction model
│   ├── `main.py`                   # FastAPI entry point
│   ├── `models.py`                 # Data schemas and validation
│   ├── `requirements.txt`          # Python dependencies
│   ├── `return_model.pkl`          # Pre-trained return forecasting model
│   ├── `utils.py`                  # Shared utility functions
│
├── 📂 data/                        # Redundant data directory (to be removed)
│   ├── 📂 processed/               # Processed and cleaned data
│   ├── 📂 raw/                     # Raw scraped data
│
├── 📂 docs/                        # Project documentation
│   ├── `Article_Scientifique.pdf`  # Scientific article on methodology
│   ├── `results.md`                # Summary of experimental results
│
├── 📂 notebooks/                   # Jupyter notebooks
│   ├── `01_scrapping.ipynb`        # Web scraping and data collection
│   ├── `02_data_collection.ipynb`  # Data cleaning and merging
│   ├── `03_feature_engineering.ipynb` # Feature engineering for models
│   ├── `04_model_training.ipynb`   # Model training and validation
│   ├── `05_mvf.ipynb`              # Portfolio optimization using MVF
│   ├── `06_predict_direction.ipynb` # Market direction prediction
│
├── `.gitignore`                    # Files ignored by Git
├── `README.md`                     # Project overview and setup instructions
├── `requirements.txt`              # Python dependencies


```
---

## 🚀 Features

### **1. Return Forecasting**:
- Train a **Random Forest model** optimized with **PSO** to predict cryptocurrency returns.
- Analyze historical market time-series data and technical indicators.

### **2. Portfolio Optimization**:
- Use **Mean-Variance Forecasting (MVF)** to compute optimal portfolio allocations.
- Evaluate portfolio performance using metrics like Sharpe ratio, volatility, and drawdown.

---

## 🔧 Technologies

- **Programming Language**: Python
- **Frameworks and Libraries**:
  - Scikit-learn: Model training and feature engineering
  - FastAPI: Serving predictions via RESTful APIs
  - Pandas, Numpy: Data preprocessing and analysis
- **Data Sources**:
  - Yahoo Finance: Historical market data
  - Other APIs: For on-chain and macroeconomic metrics

---

## 📚 Installation

### **1️⃣ Prerequisites**
- Python 3.9 or later
- Pip for dependency management

### **2️⃣ Clone the Repository**
```bash
git clone https://github.com/HELLAM1ES/crypto-forecasting-PSO-CNN.git
cd crypto-forecasting-PSO-CNN
```

### **3️⃣ Install Dependencies**
```bash
pip install -r requirements.txt
```

---

## 🛠️ Usage

### **1️⃣ Scrape Data**
Scrape cryptocurrency market data:
```bash
python crypto_api/data_processing/scrape.py
```

### **2️⃣ Merge and Process Data**
Merge raw data and create features:
```bash
python crypto_api/main.py
```
(Endpoint `/merge_and_features` in FastAPI)

### **3️⃣ Train the Model**
Train the Random Forest model:
```bash
python crypto_api/ml/train.py
```

### **4️⃣ Predict Market Direction**
Serve predictions via FastAPI:
```bash
uvicorn crypto_api.main:app --reload
```



## 📢 Contact

For any questions or suggestions, feel free to reach out to the authors:

- **Hella Bouhadda**
- **Charlotte Cegarra**
- **Chirine Doxposito**
```
