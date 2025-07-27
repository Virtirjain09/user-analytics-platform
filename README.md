# User Behavior Analytics & Churn Prediction Platform 

<p align="center">
  <img src="https://drive.google.com/file/d/18VoYf5FWtpsZREJJ3VlGVqeuXN3tS6qd/view?usp=sharing" alt="Dashboard Screenshot" width="800"/>
</p>

##  Overview

This project is an end-to-end behavioral analytics platform built to demonstrate key skills in data science and product analytics. Developed as a portfolio project at Stony Brook University, it tackles the critical business problem of user retention by providing both diagnostic insights and predictive capabilities.

The platform analyzes user event data to visualize conversion funnels, track cohort retention, and predict which users are at high risk of churning using a time-series LSTM model.

##  Key Features

* **Interactive Dashboard:** A user-friendly interface built with **Streamlit** to visualize all metrics and predictions.
* **Funnel Analysis:** Dynamically visualizes the user journey (e.g., from sign-up to upgrade) to identify the largest drop-off points.
* **Cohort Retention Analysis:** A heatmap that tracks the engagement of user cohorts over time, showing the impact of product changes on user retention.
* **Predictive Churn Model:**
    * Employs an **LSTM (Long Short-Term Memory)** model built with **Keras** to capture sequential user behavior patterns.
    * Includes a **Logistic Regression** baseline to demonstrate and quantify the superior performance of the LSTM.
    * Achieved a **28% improvement in recall**, ensuring more at-risk users are correctly identified.

##  Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Dashboard:** Streamlit
* **Visualization:** Plotly, Plotly Express
* **Machine Learning:** Scikit-learn, TensorFlow / Keras

## Setup & Installation

To run this project locally, please follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Virtirjain09/user-analytics-platform.git](https://github.com/Virtirjain09/user-analytics-platform.git)
    cd user-analytics-platform
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    # For Windows
    python -m venv venv
    .\venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## How to Run

The project must be run in the following order to generate the necessary data and model files.

1.  **Generate the mock user data:**
    ```bash
    python generate_data.py
    ```

2.  **Train the baseline and LSTM models:**
    ```bash
    python train_model.py
    ```

3.  **Launch the Streamlit application:**
    ```bash
    streamlit run app.py
    ```
    Your web browser will open with the interactive dashboard.

##  Future Improvements

* **Real-time Data Pipeline:** Connect the platform to a live database (e.g., PostgreSQL, BigQuery) to analyze events in real-time.
* **Deployment:** Deploy the Streamlit application using Streamlit Community Cloud for public access.
* **Advanced Modeling:** Experiment with more advanced sequence models like GRUs or Transformers to potentially improve predictive performance.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
