# Predicting Enzyme Activity

This project applies Machine Learning techniques to predict the enzyme activity (U/mL) of various bacterial isolates producing the amylase enzyme, based on experimental conditions: temperature (°C), pH, and starch concentration (g/L). It uses a Linear Regression model implemented in Python on Google Colab.

## Project Structure

predicting-enzyme-activity/
│
├── Predicting Enzyme Activity.ipynb  # Jupyter Notebook with code and output
├── enzyme_activity_model.pkl         # Trained Linear Regression model
├── your_dataset.csv                  # Experimental data
└── README.md                         # Project description and usage

## Dataset Description

The dataset includes enzyme assay results from 8 bacterial isolates labeled:

1A, 1B, 2C, 3A, 3B, 4A, 4B, 4C



### Column        Description

Isolate      -    Identifier of bacterial sample (categorical)

Temperature (°C)  -  Incubation temperature for enzyme activity

pH  -          pH of the medium

Starch Concentration (g/L)  -  Concentration of starch substrate

Enzyme Activity (U/mL)  -  Measured enzyme activity (target variable)


---

## Methodology

* **Data Preprocessing**: Label encoding for isolate ID, feature scaling, train-test split
* **Model**: Simple Linear Regression using `scikit-learn`
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

## Results Snapshot

* **R² Score**: *e.g., 0.89*
* **MSE**: *e.g., 1.25*

> These metrics reflect how well the model generalizes to unseen enzyme assay data.

---

## Future Enhancements

* Explore **Polynomial Regression** for non-linear patterns
* Include **interaction terms** (Temperature × pH)
* Use **cross-validation** for more robust performance evaluation
* Build a **streamlit app** to let users predict activity with a form

---

## References

* Primary data collected from enzyme assay experiments
* Research on bacterial amylase activity under varying physicochemical conditions

---

## Acknowledgments

* Conceptualized and implemented by Didhiti Dasgupta
* Guided by interest in applying ML to biotech and enzyme studies
