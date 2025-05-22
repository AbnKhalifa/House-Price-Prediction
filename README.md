# 🏠 House Price Prediction – Machine Learning Project

This project predicts house prices using regression models on the **Kaggle House Prices Dataset**, with a focus on handling skewed target variables.

---

## 📊 Problem Statement

Given features such as overall quality, living area, year built, and neighborhood, the goal is to predict the house sale price.  
**Key Improvement**: Applied log transformation to the target variable (`SalePrice`) to address skewness and improve model performance.

---

## 🧠 Models Used & Performance

| Model              | R² Score | Mean Squared Error (MSE) | Notes                              |
|--------------------|----------|--------------------------|------------------------------------|
| Linear Regression  | 0.76     | 0.04                     | Improved performance after log transformation. |
| Neural Network     | -2.4     | 0.63                     | Underperformed due to scaling/tuning issues. |
| **Random Forest**  | **0.87** | **0.02**                 | **Best model** – handles non-linear relationships effectively. |

✅ **Random Forest Regressor** outperformed others with the highest R² score and lowest MSE.

---

## 🛠️ Technologies Used

- **Python** (Pandas, NumPy, Scikit-learn)  
- **Data Visualization**: Matplotlib, Seaborn  
- **Deep Learning**: TensorFlow (for Neural Network)  
- **Notebooks**: Jupyter  

---

## 🚀 Steps Performed

1. **Data Preprocessing**:  
   - Handled missing values (e.g., imputed `GarageYrBlt` with median values).  
   - Applied **log transformation** to `SalePrice` to normalize distribution.  
   - Encoded categorical variables using **One-Hot Encoding**.  

2. **Model Training**:  
   - Split data into train/test sets (80/20 ratio).  
   - Trained Linear Regression, Neural Network, and Random Forest models.  

3. **Evaluation**:  
   - Used **R² Score**, **MSE**, and **MAE** for performance comparison.  
   - Analyzed residuals to validate log transformation effectiveness.  

---

## 📁 Project Structure

house_price_prediction/
├── data/ 
│ └── train.csv
├── notebooks/ 
│ └──  price.ipynb
├── requirements.txt 
└── README.md


---

## 🔮 Future Improvements

- **Hyperparameter Tuning**:  
  Use `RandomizedSearchCV` to optimize `max_depth` and `n_estimators` for Random Forest.  

- **Neural Network Optimization**:  
  Address scaling (e.g., StandardScaler) and test architectures (e.g., dropout layers).  

- **Feature Engineering**:  
  Explore interaction terms (e.g., `TotalSF = GrLivArea + TotalBsmtSF`).  

- **Deployment**:  
  Build a Streamlit app for real-time predictions.  

- **Explainability**:  
  Generate SHAP plots to interpret Random Forest decisions.  

---

## 👨💻 Author

**Adham Khalifa**  
📫 [LinkedIn](https://www.linkedin.com/in/abn-khalifa)  
💻 [GitHub](https://github.com/AbnKhalifa/house_price_prediction)  

---

## 📄 License

This project is open source under the [MIT License](LICENSE).