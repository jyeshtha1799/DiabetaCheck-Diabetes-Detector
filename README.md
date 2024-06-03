# DiabetaCheck-Diabetes-Detector


This Flask application utilizes a machine learning model to predict diabetes based on health metrics provided by users through a web interface. It incorporates data preprocessing, visualization, and machine learning model training to deliver a prediction on whether a user is likely to have diabetes.

## Project Structure

Below is the structure and description of the main components in this project:

- **main.py**: Flask application for handling routes and rendering templates.
- **ModelPrep.ipynb**: Jupyter notebook for preparing and training the SVM model.
- **null.ipynb**: Jupyter notebook for handling missing values in the dataset.
- **visualiz.ipynb**: Jupyter notebook for data visualization and analysis.
- **svm_model.pkl**: Serialized file of the trained SVM model.
- **templates/**: Folder containing HTML templates for the web interface.
  - **home.html**: Form for inputting health metrics.
  - **show.html**: Display results of the diabetes prediction.
- **diabetes.csv**: Dataset used for training the machine learning model.

## Installation

To run this project locally, follow these steps:

1. **Clone the Repository:**
   ```
   git clone https://github.com/jyeshtha1799/DiabetaCheck-ML-Diabetes-Detector.git
   cd diabetes-prediction-flask
   ```

2. **Set Up a Virtual Environment** (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies:**
   ```
   pip install flask pandas numpy scikit-learn matplotlib seaborn plotly jupyter
   ```

4. **Start the Application:**
   ```
   python main.py
   ```
   This will run the Flask server.

## Usage

- **Access the Application**: Open a browser and navigate to `http://localhost:5000` to use the diabetes prediction form.
- **Enter Health Metrics**: Fill out the form with health metrics such as glucose level, blood pressure, etc., and submit.
- **View Prediction**: The prediction result will be displayed on a new page, indicating the likelihood of diabetes.

## Contributing

Contributions to the project are welcome. You can enhance functionality, add new features, improve the UI, or address existing bugs. Please fork the repository and submit a pull request with your changes.

