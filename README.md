#### 0====No Heart Disease
#### 1====Heart Disease
#### gunicorn -w 4 -b 0.0.0.0:8000 app:flask_app

#### Please read this carefully for accurate prediction of heart disease.

***df['heart_disease'] = df['heart_disease'].replace({'Yes': 1, 'No': 0})***

***df['kidney_disease'] = df['kidney_disease'].replace({'Yes': 1, 'No': 0})***

***df['skin_cancer'] = df['skin_cancer'].replace({'Yes': 1, 'No': 0})***

***df['smoking'] = df['smoking'].replace({'Yes': 1, 'No': 0})***

***df['asthma'] = df['asthma'].replace({'Yes': 1, 'No': 0})***

***df['alcohol_drinking'] = df['alcohol_drinking'].replace({'Yes': 1, 'No': 0})***

***df['stroke'] = df['stroke'].replace({'Yes': 1, 'No': 0})***

***df['physical_activity'] = df['physical_activity'].replace({'Yes': 1, 'No': 0})***

***df['diff_walking'] = df["diff_walking"].replace({'Yes': 1, 'No': 0})***

***df['sex'] = df["sex"].replace({'Male': 1, 'Female': 0})***

***df["age_category"]=df["age_category"].replace({ '18-24': 0,'25-29': 1,'30-34': 2,'35-39': 3,
                                                                                    '40-44': 4,
                                                                                    '45-49': 5,
                                                                                    '50-54': 6,
                                                                                    '55-59': 7,
                                                                                    '60-64': 8,
                                                                                    '65-69': 9,
                                                                                    '70-74': 10,
                                                                                    '75-79': 11,
                                                                                    '80 or older': 12})***

***df["race"]=df["race"].replace({"White":0,"Hispanic":1,"Black":3,"Asian":4,"American Indian/Alaskan Native":5,"Other":6})***

***df["gen_health"]=df["gen_health"].replace({"Very good":0,"Good":1,"Excellent":3,"Fair":4,"Poor":5})***

***df['diabetic'] = df['diabetic'].replace({'Yes': 1, 'No': 0,"No, borderline diabetes":0,"Yes (during pregnancy)":1})***


### Details About requirements.txt

#### Flask==3.0.3: Flask is a popular web framework for Python used for building web applications. This line specifies that the version 3.0.3 of Flask is required. Flask is used for handling HTTP requests, routing, and rendering HTML templates, among other things.

#### numpy==1.26.4: NumPy is a fundamental package for scientific computing with Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of mathematical functions to operate on these arrays. This line specifies that version 1.26.4 of NumPy is required.

#### scikit-learn==1.4.2: Scikit-learn is a machine learning library for Python. It provides simple and efficient tools for data mining and data analysis, including classification, regression, clustering, dimensionality reduction, and more. This line specifies that version 1.4.2 of scikit-learn is required.

#### scipy==1.13.0: SciPy is a library used for scientific and technical computing. It builds on NumPy and provides a large number of functions that operate on numpy arrays and are useful for different types of scientific and engineering applications. This line specifies that version 1.13.0 of SciPy is required.

#### gunicorn==21.2.0: Gunicorn is a WSGI HTTP server for Python. It is commonly used to deploy Python web applications, including those built with Flask. Gunicorn is known for its speed, scalability, and simplicity. This line specifies that version 21.2.0 of Gunicorn is required.


### Flask Application (app.py):

***app.py serves as the main script for your Flask application. It initializes the Flask app, defines routes, and handles requests.
Routes are defined to render the home page (index.html) and handle prediction requests.
Prediction requests are processed using a machine learning model integrated into the Flask app.
Results are displayed to the user after prediction.***

### HTML Template (index.html):

***index.html is located in the templates folder, which is a convention for Flask applications to serve HTML files.
It provides the user interface for interacting with the heart disease prediction application.
Input fields, such as age, gender, and medical history, are included to collect necessary data for prediction.
Upon submission, the form data is sent to the Flask backend for processing.***

## Deployment:

### Render Web Service:

***The Flask application is deployed on a web service platform like Render.
Render provides scalable cloud hosting for web applications, making it suitable for deploying Flask applications.
Deployment involves configuring the environment, setting up dependencies, and deploying the Flask app.
The heart disease prediction application becomes accessible via a URL provided by the Render web service.***

### Functionality:

***Users access the heart disease prediction application through a web browser.They input relevant information such as age, gender, and medical history into the provided form.Upon submission, the Flask backend processes the input data, predicts the likelihood of heart disease using the integrated machine learning model, and returns the result.Users receive the prediction output on the web page, along with any additional information or recommendations provided by the application.***

