# Module 21 Challenge - SMS Spam Detector

## Description

This project involves refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. The model is trained to classify SMS messages as either spam or not spam. The application is hosted using Gradio, enabling users to test text messages through a web interface.

## Files

- `gradio_sms_text_classification.ipynb`: The Jupyter Notebook containing the implementation of the SMS spam detection model and the Gradio app.
- `sms_text_classification_solution.ipynb`: The original solution notebook used to create the SMS classification function.
- `SMSSpamCollection.csv`: The dataset containing labeled SMS messages used to train and test the model.

## Requirements

- Python 3.x
- pandas
- scikit-learn
- gradio

## Usage

- Run the Jupyter Notebook gradio_sms_text_classification.ipynb to train the model and launch the Gradio app. 
- Open the provided URL to access the Gradio interface.
- Enter a text message in the input box and see the classification result.

## Challenge Instructions
Create the SMS Classification Function

- Set the features variable to the text message column of the DataFrame.
- Set the target variable to the "label" column of the DataFrame.
- Split data into training and testing sets, with the test size set to 33%.
- Build a pipeline to transform the test set to compare to the training set.
- Fit the model to the transformed training data and return the model.
- Load the SMSSpamCollection.csv into a DataFrame and call the sms_classification function with the DataFrame, setting the result to the "text_clf" variable.

Create the SMS Prediction Function

- Create a variable that holds the prediction of a new text.
- Use a conditional statement to determine if the text message is "ham" or "spam".
- If the message is "ham", the function should return: f'The text message: "{text}", is not spam.'
- If the message is "spam", the function should return: f'The text message: "{text}", is spam.'

Create the Gradio Interface Application

- Create a Gradio Interface application with three parameters: function, outputs, and inputs.
- The outputs parameter is a textbox that contains a label to let the user know what to type in the box.
- The inputs parameter is a textbox that contains a label to let the user know that the prediction will be displayed in the textbox.
- Launch the application and provide the URL to share the application.

Example Messages for Testing

- You are a lucky winner of $5000!
- You won 2 free tickets to the Super Bowl.
- You won 2 free tickets to the Super Bowl. Text us to claim your prize.
- Thanks for registering. Text 4343 to receive free updates on Medicare.
