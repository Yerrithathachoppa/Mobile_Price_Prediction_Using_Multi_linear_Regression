# 📱 Mobile Price Prediction

A machine learning project that predicts mobile phone prices based on hardware specifications using Linear Regression.

## 📊 Project Overview

This project analyzes mobile phone specifications and builds a predictive model to estimate prices. Using data-driven insights and correlation analysis, we demonstrate that simple Linear Regression achieves excellent performance (R² = 0.96) for this problem.

## 🎯 Objective

Predict mobile phone prices based on hardware features such as:
- RAM
- Internal Memory
- CPU specifications (cores, frequency)
- Display quality (PPI, resolution)
- Camera quality (rear and front)
- Battery capacity
- Physical attributes (weight, thickness)

## 📁 Dataset

**Source**: [Kaggle - Mobile Price Prediction](https://www.kaggle.com/datasets/mohannapd/mobile-price-prediction)  
**Author**: Fatemeh.V.Younesi  
**License**: [CC0 Public Domain](https://creativecommons.org/publicdomain/zero/1.0/)  

- **File**: `Cellphone.csv`
- **Records**: 162 mobile phones
- **Features**: 14 columns (12 after preprocessing)
- **Target Variable**: Price (in ₹)

*This dataset is released under CC0 Public Domain license, allowing free use, modification, and distribution without restrictions.*

### Features Description

| Feature | Description |
|---------|-------------|
| Product_id | Product identifier (removed during preprocessing) |
| Price | Phone price in ₹ (target variable) |
| Sale | Sales volume (removed - data leakage) |
| weight | Phone weight in grams |
| resoloution | Screen size in inches |
| ppi | Pixels per inch (screen quality) |
| cpu core | Number of CPU cores |
| cpu freq | CPU frequency in GHz |
| internal mem | Internal storage in GB |
| ram | RAM in GB |
| RearCam | Rear camera megapixels |
| Front_Cam | Front camera megapixels |
| battery | Battery capacity in mAh |
| thickness | Phone thickness in mm |

## 🔍 Key Findings

### Strong Price Predictors (Correlation)
1. **RAM (0.90)** - Strongest predictor
2. **PPI (0.82)** - Screen quality matters
3. **Internal Memory (0.78)** - Storage capacity
4. **Rear Camera (0.74)** - Camera quality
5. **CPU Frequency (0.73)** - Processing power
6. **CPU Cores (0.69)** - Multi-core performance
7. **Thickness (-0.72)** - Thinner phones cost more (negative correlation)

### Model Performance

**Linear Regression Results:**
- **Training R² Score**: 0.9507
- **Testing R² Score**: 0.9588
- **Training RMSE**: ₹170.68
- **Testing RMSE**: ₹152.83

**Interpretation**: The model explains 95.88% of price variation, with predictions accurate within ~₹153 on average.

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation
- **numpy** - Numerical operations
- **matplotlib** - Data visualization
- **seaborn** - Statistical visualizations
- **scikit-learn** - Machine learning
- **scipy** - Statistical analysis

## 📦 Installation

### Prerequisites
```bash
Python 3.7+
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Required Packages
```
pandas
numpy
matplotlib
seaborn
scikit-learn
scipy
```

## 🚀 Usage

1. **Clone the repository**
```bash
git clone <repository-url>
cd Mobile_Price_Prediction
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the Jupyter Notebook**
```bash
jupyter notebook Model.ipynb
```

4. **View the Gradient Descent Animation**
- The project includes `gradient_descent_animation.gif` showing how the regression line converges

## 📓 Notebook Structure

1. **Data Loading & Exploration**
   - Load dataset
   - Check for missing values
   - Statistical summary

2. **Exploratory Data Analysis**
   - Feature vs Price scatter plots
   - Correlation heatmap analysis
   - Distribution analysis

3. **Data Preprocessing**
   - Remove Product_id (identifier only)
   - Remove Sale (data leakage)
   - Verify data quality

4. **Model Building**
   - Train-test split (80-20)
   - Linear Regression training
   - Model predictions

5. **Model Evaluation**
   - R² Score
   - RMSE calculation
   - Actual vs Predicted plots
   - Residual analysis
   - Feature importance

## 📈 Visualizations

The project includes several insightful visualizations:
- **Scatter plots** with regression lines showing feature-price relationships
- **Correlation heatmap** revealing feature dependencies
- **Actual vs Predicted** plot demonstrating model accuracy
- **Residual plot** showing prediction errors
- **Gradient descent animation** (GIF) showing optimization process

## 🎓 Machine Learning Approach

### Why Linear Regression?

Based on exploratory analysis:
1. **Linear relationships** between features and price
2. **High correlations** (>0.7) with target variable
3. **Interpretability** - clear coefficient meanings
4. **Excellent performance** - R² > 0.95

### Model Interpretation

**Top Feature Coefficients:**
- **CPU Frequency**: +₹128.43 per GHz
- **RAM**: +₹109.51 per GB
- **CPU Cores**: +₹50.56 per core
- **Thickness**: -₹71.27 per mm (thinner = more expensive)

## 🔮 Future Improvements

1. **Larger Dataset** - Current dataset has only 162 records
2. **Brand Information** - Include manufacturer as a feature
3. **Ensemble Methods** - Try Random Forest, Gradient Boosting
4. **Feature Engineering** - Create composite features
5. **Time Series** - Include launch year/date
6. **Web Scraping** - Collect more recent data
7. **Model Deployment** - Create web API for predictions

## ⚠️ Limitations

- Small dataset (162 phones)
- Missing brand/manufacturer information
- No temporal data (year of release)
- Possible selection bias in data collection
- "resoloution" column has typo (should be "resolution")

## 📊 Project Structure

```
Mobile_Price_Prediction/
├── Model.ipynb                          # Main Jupyter notebook
├── Cellphone.csv                        # Dataset
├── gradient_descent_animation.gif       # Optimization visualization
├── mobile_price_model.pkl               # Trained model
├── requirements.txt                     # Python dependencies
├── README.md                           # Project documentation
├── .gitignore                          # Git ignore rules
└── LICENSE                             # MIT License
```

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 👤 Author

Created as a machine learning practice project demonstrating:
- Data analysis and visualization
- Feature selection and correlation analysis
- Linear regression modeling
- Model evaluation and interpretation

## 📧 Contact

For questions or feedback, please open an issue in the repository.

---

**Note**: This is an educational project demonstrating linear regression for price prediction. The model achieves excellent performance on this specific dataset but should be validated with additional data before production use.
