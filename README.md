# Global Street Food Cooking Method Prediction
# How you want to cook your food? 😋

1. Pre-processing

Welcome to the **Global Street Food Cooking Method Prediction** project!  
This repository demonstrates a full machine learning workflow to predict the cooking method of street foods from their ingredients, description, and vegetarian status.

---

## 📋 Project Overview

This project uses a dataset of global street foods to build a model that predicts the cooking method (e.g., frying, steaming, baking) based on:
- **Ingredients**
- **Description**
- **Vegetarian status**

The workflow includes:
1. Data loading and exploration
2. Pre-processing and feature engineering
3. Model training (TensorFlow/Keras)
4. Evaluation and visualization
5. Interactive prediction

---

## 🗂️ Folder Structure

```
.
├── global_street_food.csv
├── 1_Data.ipynb
├── street_food_model.h5
├── label_encoder.pkl
├── tfidf_vectorizer.pkl
└── README.md
```

---

## 🚀 How It Works

### 1. Data Preparation
- Load and clean the dataset (`global_street_food.csv`)
- Explore distributions of cooking methods, countries, and vegetarian status

### 2. Feature Engineering
- Use **TF-IDF vectorization** for both Ingredients and Description
- Encode Vegetarian status as binary
- Concatenate all features for model input

### 3. Model Training
- Split data into train/test sets
- Build a neural network using TensorFlow/Keras
- Train and save the model (`street_food_model.h5`)

### 4. Evaluation
- Print accuracy and loss
- Visualize training/validation curves
- Show classification report and confusion matrix

### 5. Prediction
- Load the trained model and encoders
- Transform new inputs using saved TF-IDF vectorizer and label encoder
- Pad features if needed to match model input size
- Predict and display the cooking method

---

## 🧑‍💻 Usage

1. **Clone the repository**
2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib scikit-learn tensorflow
   ```
3. **Run the Jupyter notebook**
   - Open `1_Data.ipynb` in VS Code or Jupyter
   - Follow the cells step-by-step

4. **Interactive Prediction**
   - Use the provided function to predict cooking method for any street food by entering its ingredients, description, and vegetarian status.

---

## 📊 Example Output

```
Enter the street food name: Noodles
Enter the ingredients: Wheat flour, water, salt
Enter the description: Thin strands boiled and served with sauce
Is it vegetarian? (Yes/No): Yes
You should cook 'Noodles' using the 'Boiling' method.
```

---

## 📝 Notes

- The model expects input features of a specific size; padding is used if the TF-IDF output is shorter.
- The label encoder maps numeric predictions back to actual cooking method names.
- For best results, use the same pre-processing steps for new data as in training.

---

## 📚 References

- [Scikit-learn documentation](https://scikit-learn.org/)
- [TensorFlow documentation](https://www.tensorflow.org/)
- [TF-IDF Vectorization](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)

---

## 🏆 License

This project is for educational purposes.  
Feel free to fork, modify, and share!

---
