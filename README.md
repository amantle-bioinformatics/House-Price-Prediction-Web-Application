# Housing Price Prediction & Web Deployment

This project is a comprehensive end-to-end data science application designed to predict house prices based on various features such as area, number of bedrooms, bathrooms, and additional amenities. It includes a machine learning model built with Python and a web-based user interface for real-time predictions.

**My successfully deployed web app link**: https://amantlemhouse-price-prediction-web-application-7vgsmbeesf8rvdb.streamlit.app/

## 📈 Project Workflow
The project follows a structured 6-step pipeline:

***Dataset**: Sourcing and understanding the Housing.csv data.
***Data Cleaning**: Handling missing values, outliers, and encoding categorical variables (e.g., converting "yes/no" to numerical values).
***Model Training**: Training a regression model (such as Linear Regression or Random Forest) using Scikit-Learn.
***Save Model**: Exporting the trained model using pickle or joblib for future use.
***Build Web App**: Developing an interactive user interface using Streamlit.
***Deploy**: Hosting the application (e.g., on Streamlit Cloud or Render) so users can access it via a URL.

---

## 📊 Dataset Description

The dataset (`Housing.csv`) contains **545 records** with the following features:

| Column Name | Description | Type |
| --- | --- | --- |
| `price` | The target variable (Target Price in USD/Local Currency). | Numeric |
| `area` | Total area of the house in square feet. | Numeric |
| `bedrooms` | Number of bedrooms. | Numeric |
| `bathrooms` | Number of bathrooms. | Numeric |
| `stories` | Number of floors in the house. | Numeric |
| `mainroad` | Whether the house is on the main road (yes/no). | Categorical |
| `guestroom` | Presence of a guest room (yes/no). | Categorical |
| `basement` | Presence of a basement (yes/no). | Categorical |
| `hotwaterheating` | Presence of hot water heating (yes/no). | Categorical |
| `airconditioning` | Presence of air conditioning (yes/no). | Categorical |
| `parking` | Number of parking spots available. | Numeric |
| `prefarea` | Whether the house is in a preferred area (yes/no). | Categorical |
| `furnishingstatus` | Status of furnishing (furnished, semi-furnished, unfurnished). | Categorical |

---

## 🛠️ Tech Stack

* **Language**: Python 3.x
* **Data Analysis**: Pandas, NumPy
* **Machine Learning**: Scikit-learn (Linear Regression, Random Forest, etc.)
* **Save Model**: Pickle or Joblib
* **Web Framework**: [Streamlit](https://streamlit.io/) (Recommended for beginners) or Flask
* **Environment**: Jupyter Notebook/Google Colab (for Cleaning and Training) and Streamlit Cloud or Render (for Deployment)

---

## 📂 Project Structure

```text
├── data/
│   └── Housing.csv             # Raw dataset
├── models/
│   └── house_model.pkl         # Saved trained model
├── app.py                      # Streamlit/Web application code
├── requirements.txt            # List of libraries to install
└── README.md                   # Project documentation

```

---

## 💡 Key Learnings for Beginners

* **Handling Categorical Data**: Use `pd.get_dummies()` or `LabelEncoder` to convert "yes/no" into 1s and 0s so the computer can understand them.
* **Model Evaluation**: We use **Mean Absolute Error (MAE)**  to check how accurate our price predictions are.
* **Model Persistence (The "Pickle" Moment)**:This is often the biggest hurdle for beginners moving to web development. In Colab, the model lives in the computer's temporary memory. Once you close the tab, the model is gone. The Solution is you learn how to Serialize (save) your model as a .pkl file. This teaches you that a Machine Learning model is just a "weight file" that can be moved from the cloud (Colab) to a local app (Streamlit).
* **Designing for the User (Web UI)**: When you build the web app, you stop thinking like a mathematician and start thinking like a developer. A user won't type 1 for "Yes" and 0 for "No." You learn to build Input Widgets (dropdowns and sliders) that translate user-friendly choices back into the binary data your model expects.


