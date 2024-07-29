# sms_spam_detector
Constructs a linear Support Vector Classification (SVC) model Classifying if an email is SPAM or HAM
# SMS Spam Detector

## Background
This project involves refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, you will create a Gradio app to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not based on the model's performance.

## Files
Download the following files to get started:

- [Module 21 Challenge files](https://static.bc-edx.com/ai/ail-v-1-0/m21/challenge/files.zip)

## Before You Begin
1. Create a new repository for this project called `sms_spam_detector`. Do not add this assignment to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local Git repository, add the starter files from your file downloads.
4. Push these changes to GitHub or GitLab.

## Challenge Instructions
The starter files consist of the following files:
- `gradio_sms_text_classification.ipynb`
- `sms_text_classification_solution.ipynb`
- `SMSSpamCollection.csv`

### Create the SMS Classification Function
Using the code in the `sms_text_classification_solution.ipynb` file, create the `sms_classification` function in the `gradio_sms_text_classification.ipynb` by following these steps:

1. Set the `features` variable to the text message column of the DataFrame.
2. Set the `target` variable to the "label" column of the DataFrame.
3. Split the data into training and testing sets with `test_size` set to 33%.
4. Build a pipeline to transform the test set to compare to the training set.
5. Fit the model to the transformed training data and return the model.
6. Load the `SMSSpamCollection.csv` into a DataFrame and call the `sms_classification` function with the DataFrame, setting the result to the `text_clf` variable.

### Create the SMS Prediction Function
Use the `sms_prediction` function to predict the classification of a new text by following these steps:

1. Create a variable that will hold the prediction of a new text.
2. Use a conditional statement to determine if the text message is "ham" or "spam".
3. If the message is "ham", the function should return the following message: `f'The text message: "{text}", is not spam.'`
4. If the message is "spam", the function should return the following message: `f'The text message: "{text}", is spam.'`

### Create the Gradio Interface Application
Create a Gradio Interface application that:

1. Takes a textbox for the input and has a textbox for the output.
2. Labels the textboxes to describe their content.
3. Launch the application and provide the URL to share the application.

The application should look like this:

![The SMS prediction Gradio application interface](https://static.bc-edx.com/ai/ail-v-1-0/m21/challenge/sms_gradio_app.png)

### Test Messages
Use the following text messages to test your application:
1. You are a lucky winner of $5000!
2. You won 2 free tickets to the Super Bowl.
3. You won 2 free tickets to the Super Bowl. Text us to claim your prize.
4. Thanks for registering. Text 4343 to receive free updates on Medicare.



## Acknowledgements
- Dataset provided by [Module 21 Challenge](https://static.bc-edx.com/ai/ail-v-1-0/m21/challenge/files.zip).

## Requirements
- Python 3.x
- Pandas
- Scikit-learn
- Gradio
