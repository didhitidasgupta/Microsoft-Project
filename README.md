# Predicting Enzyme Activity

This project applies Machine Learning techniques to predict the enzyme activity (U/mL) of various bacterial isolates producing the amylase enzyme, based on experimental conditions: temperature (°C), pH, and starch concentration (g/L). It uses a Linear Regression model implemented in Python on Google Colab.

## Project Structure

 * Predicting Enzyme Activity.ipynb: Using Google Colab

 * enzyme_activity_model.pkl: Trained Linear Regression model

 * enzyme_activity.csv: Experimental data

 * README.md: Project description and usag

## Dataset Description

The dataset includes enzyme assay results from labeled bacterial isolates.

### Column        Description

Isolate      -    Identifier of bacterial sample (categorical)

Temperature (°C)  -  Incubation temperature for enzyme activity

pH  -          pH of the medium

Starch Concentration (g/L)  -  Concentration of starch substrate

Enzyme Activity (U/mL)  -  Measured enzyme activity (target variable)

---

## Methodology

* **Data Preprocessing**: Label encoding for isolate ID, feature scaling, train-test split
* **Model**: Simple Linear Regression
* **Evaluation Metrics**:
  * Mean Squared Error (MSE)
  * R² Score
* **Visualization**: Scatter plot comparing actual vs predicted activity

---

## How to Run

1. **Google Colab**: Open [`Predicting Enzyme Activity.ipynb`](Predicting Enzyme Activity.ipynb) in Colab
2. **Upload dataset**:
   * Upload the CSV manually or mount Google Drive
3. **Install requirements**:
   * All dependencies are standard: `pandas`, `sklearn`, `matplotlib`, `seaborn`
4. **Run cells** to preprocess, train, evaluate, and visualize model

---

## Results

* **R² Score**: *0.7016*
* **Mean Squared Error**: *0.0245* 

> These metrics reflect how well the model generalizes to unseen enzyme assay data.

---

## 3D surface plot of Enzyme Activity vs Temperature and pH. 
This will give us a better sense of their combined effect. This visualization helps in understanding the relationship between these three variables in a three-dimensional space.

---

## Deployment

**Save the trained model**: Use a library like joblib to save the trained LinearRegression model to a file.
**Load the saved model**: Load the saved model from the file.
**Prepare new data for prediction**: Create a new DataFrame with the same structure as the training data (including one-hot encoded 'Isolate' columns) but containing the data for which you want to make predictions.
**Make predictions on new data**: Use the loaded model to make predictions on the prepared new data.
**Display predictions**: Show the predicted enzyme activity for the new data.

## References

* Primary data collected from enzyme assay experiments
* Research on bacterial amylase activity under varying physicochemical conditions

---

## Acknowledgments

* Conceptualized and implemented by Didhiti Dasgupta
* Guided by interest in applying ML to biotech and enzyme studies
