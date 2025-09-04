🌲 Forest Cover Type Classification using XGBoost

This project applies multi-class classification using XGBoost to predict the type of forest cover from cartographic and environmental features.

📌 Objective

- Use the [Covertype Dataset (UCI)
- Predict the forest cover type (7 categories) using environmental features
- Apply tree-based classification (XGBoost)
- Evaluate using metrics for multi-class classification
- Visualize confusion matrix and feature importance

📊 Dataset Overview

The dataset contains over 500,000 entries with 54 features:

- Numerical Features: Elevation, Slope, Soil Type, Aspect, etc.
- Categorical Features: Wilderness_Area and Soil_Type (one-hot encoded)
- Target Variable: `Cover_Type` (values 1–7, converted to 0–6)

➡️ Multi-class classification problem with 7 forest types

🧰 Tools & Libraries

- Python 
- pandas
- scikit-learn
- XGBoost
- seaborn + matplotlib (for visualizations)

🔍 Steps Performed

1. Data Loading: Loaded CSV file using pandas
2. Target Adjustment: Shifted `Cover_Type` values from 1–7 to 0–6
3. Train/Test Split: Stratified 80/20 split
4. Model Training:
   - Used `XGBClassifier` with `multi:softmax` objective
   - Enabled `use_label_encoder=False`
5. Predictions: Predicted on test set
6. Evaluation:
   - Accuracy Score
   - Confusion Matrix (visualized)
   - Classification Report (optional)
7. Feature Importance: Plotted top contributing features

📈 Results

Model achieved high accuracy on multi-class prediction with well-separated confusion matrix.

Confusion Matrix revealed:
- Some misclassification between similar cover types (e.g., 2 vs 3)
- Most dominant classes were predicted accurately

🧠 Key Takeaways

- XGBoost handles large, high-dimensional datasets efficiently
- Multi-class classification works well with tree-based models
- Confusion matrix helps spot class-wise weaknesses
- Feature importance highlights what matters most for prediction

✅ Future Improvements

- Use cross-validation for more robust evaluation
- Apply dimensionality reduction (PCA) to visualize clusters
- Test alternate models: Random Forest, LightGBM, CatBoost
- Fine-tune using GridSearchCV

👨‍💻 Author

Muhammad Mustaqeem Javed — AI/ML Intern  
