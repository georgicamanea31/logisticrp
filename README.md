# Logistic Regression for Breast Cancer Classification

## Project Overview  
This project applies **logistic regression** to classify breast cancer tumors as malignant (M) or benign (B) using the **Breast Cancer Wisconsin Dataset**. The goal is to build a predictive model that can help in early diagnosis by analyzing tumor characteristics.

## Dataset Description  
The dataset contains various numerical features extracted from digitized images of breast mass cell nuclei. Each sample is labeled as either **Malignant (M)** or **Benign (B)** under the `diagnosis` column.  

### Data Preprocessing Steps  
1. **Loading the Dataset**  
   - The data is read from a CSV file using `pandas`.  
2. **Exploratory Data Analysis (EDA)**  
   - First five rows are displayed using `.head()`.  
   - Dataset information and summary statistics are extracted using `.info()` and `.describe()`.  
3. **Cleaning Data**  
   - Dropping unnecessary columns (`Unnamed: 32`, `id`).  
   - Converting the categorical **diagnosis** column into binary values:  
     - `M` → 1 (Malignant)  
     - `B` → 0 (Benign)  
   - Visualizing class distribution using a **bar plot**.  
4. **Feature Selection**  
   - The target variable `y` is set as the `diagnosis` column.  
   - The features `X` include all remaining columns except `diagnosis`.  
5. **Feature Scaling**  
   - Standardizing the features using **StandardScaler** to improve model performance.  

### Model Training and Evaluation  
1. **Splitting Data**  
   - The dataset is split into **70% training** and **30% testing** using `train_test_split()`.  
2. **Training Logistic Regression**  
   - A **Logistic Regression** model is instantiated and trained using `X_train` and `y_train`.  
3. **Predictions and Evaluation**  
   - The model predicts outcomes on `X_test`.  
   - **Accuracy Score** is calculated to measure performance.  
   - A **classification report** is generated, displaying:  
     - **Precision** (How many selected items are relevant)  
     - **Recall** (How many relevant items were selected)  
     - **F1-score** (Balance between precision and recall)  

### Results  
The model achieves an accuracy of around **X%** (depends on dataset). The classification report provides detailed insights into model performance.

## Conclusion  
Logistic Regression proves to be an effective technique for breast cancer classification with a decent accuracy score. Further improvements can be made by trying other models like **Random Forest, SVM, or Neural Networks**, and applying feature selection techniques.

---

### Dependencies  
To run this project, install the following Python libraries:  

```bash
pip install pandas seaborn scikit-learn matplotlib
