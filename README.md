## Diabetes Prediction System - Detailed ReadMe

This README provides a comprehensive guide to the Diabetes Prediction System. This project is an end-to-end machine learning application designed to predict diabetes based on user-provided health metrics. The system is built using Python, Flask, and various machine learning models, and it offers an interactive user interface where users can input their health data and receive predictions on their diabetes risk.

### Project Structure Overview
- `main.py`: Main Flask application script that configures and runs the web server.
- `modelPrep.ipynb`: Jupyter Notebook for preparing the data, including cleaning and feature selection.
- `null.ipynb`: Jupyter Notebook focused on handling missing data values and feature engineering.
- `visualiz.ipynb`: Jupyter Notebook for visualizing the data to understand distributions and relationships between features.
- `templates/`: Folder containing HTML templates for the web interface, including the data input form and the prediction results page.


### Installation and Setup
1. **Environment Preparation**:
   - Ensure Python 3.x is installed along with pip.
   - Install all necessary Python libraries by running: `pip install flask pandas numpy scikit-learn matplotlib seaborn`.

2. **Running the Application**:
   - Open a terminal and navigate to the project directory.
   - Execute `python main.py` to initiate the Flask server.
   - Open a web browser and go to `http://localhost:5000` to interact with the application.


### Data Visualization and Cleaning
- **Scatter Plots and Histograms**: Used to examine relationships between variables and identify outliers. Visualizations highlight key features that influence diabetes outcomes.
![image](https://github.com/jyeshtha1799/DiabetaCheck-ML-Diabetes-Detector/assets/114448454/61578d99-f814-4f7d-98d0-cbd0945e64b6)
- **Correlation Matrix**: Helps identify highly correlated features which might affect model performance. 
![image](https://github.com/jyeshtha1799/DiabetaCheck-ML-Diabetes-Detector/assets/114448454/e2b31192-af0a-48ec-983a-5700a4ad1b6f)

- **Handling Missing Data**: Techniques include replacing zero values that represent missing data with NaN, followed by median imputation based on the outcome variable to preserve data integrity without skewing distribution.
![image](https://github.com/jyeshtha1799/DiabetaCheck-ML-Diabetes-Detector/assets/114448454/8081a090-1ac4-4c9b-8e2c-3e7117db8ed7)


### Feature Engineering Details
- **Imputation Strategy**: Median values are calculated separately for diabetic and non-diabetic groups to tailor the data imputation to different patterns observed in these groups. This method helps in maintaining the clinical validity of the model.
- **Standardization**: All numeric features are scaled to have a mean of zero and a standard deviation of one. This step is crucial for models like SVM and KNN to function correctly and efficiently.


### Model Training and Evaluation
- **Model Selection**: Several models were evaluated, including logistic regression, K-Nearest Neighbors, Support Vector Machines (SVM), Random Forest, and a Sequential Neural Network. Each model's performance was assessed based on accuracy, precision, and recall.
- **Model Optimization**: The SVM model demonstrated the highest overall accuracy and was selected for deployment. Details about the model's configuration and the rationale behind choosing SVM are documented in `modelPrep.ipynb`.


### Web Interface and Flask Deployment
- **HTML Forms**: The `home.html` template collects input from users, such as glucose levels, blood pressure, and other health metrics. CSS is used to enhance the form's appearance, making it intuitive and accessible.
- **Result Display**: The `show.html` template presents the model's prediction in a clear and understandable manner, informing the user whether they are predicted to be diabetic or not.
- **Flask Routing**: Flask routes handle the form data submission (`/send` route), process it through the model, and render the prediction results on the `show.html` page.


### Conclusion and Future Directions
This application exemplifies how machine learning can be applied to real-world health issues, providing a tool for non-technical users to assess their risk of diabetes. Future enhancements could include integrating more complex models, expanding the feature set, or adapting the application for other health conditions.

