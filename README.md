# 🧠 Alzheimer Prediction using MLP Classifier

This project leverages the OASIS cross-sectional dataset to predict dementia in patients using clinical features. It involves data preprocessing, feature analysis, model training using a Multi-Layer Perceptron (MLP), and visual evaluation using various metrics.

## 📁 Dataset
- **Source**: [OASIS: Open Access Series of Imaging Studies](https://www.oasis-brains.org/)
- The dataset includes features like Age, Education Level, SES, MMSE, eTIV, nWBV, and ASF.
- A binary target column `Label` is generated from `CDR` where:
  - `CDR > 0 → Demented (1)`
  - `CDR = 0 → Non-Demented (0)`

## 🧪 Technologies Used
- `Pandas`, `NumPy` for data manipulation
- `Scikit-learn` for model training and evaluation
- `Matplotlib`, `Seaborn` for visualization
- `MLPClassifier` for binary classification

## 📊 Steps Performed
- Loaded and preprocessed the dataset (filled missing values, created labels)
- Split data into training and testing sets
- Standardized features using `StandardScaler`
- Trained a neural network using `MLPClassifier`
- Evaluated model with:
  - Accuracy score
  - Confusion matrix
  - Classification report
  - Visualizations (feature distributions, heatmaps)

## 🤖 Predict New Patient
A custom `predict_new_data()` function allows prediction on new clinical input data, returning both class label and probability.

```python
predict_new_data(age=75, educ=4, ses=2, mmse=28, etiv=1500, nwbv=0.7, asf=1.1)
# Output:
# Predicted Label: Non-Demented
# Probability of Dementia: 0.14
```

📷 Visualizations
- Target label distribution
- Histograms of each feature by dementia label
- Correlation heatmap
- Confusion matrix

📈 Accuracy
- Accuracy on test data: ~[add accuracy here]
- Detailed classification report printed in console

🛠️ How to Run
1. Install dependencies: ``` pip install pandas scikit-learn matplotlib seaborn openpyxl ```
2. Place the dataset file as oasis_cross-sectional-5708aa0a98d82080.xlsx
3. Run the script in a Jupyter notebook or Python environment.

📂 Output
Saves a labeled version of the dataset as oasis_cross-sectional_labeled.xlsx
