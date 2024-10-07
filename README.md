# SMS Spam Detector

This is the Module 21 Challenge.

## Background

This project involves refactoring a codebase for an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, a Gradio app will be developed to allow users to test text messages, providing feedback on whether the text is classified as spam or not.

## Project Structure

The project includes the following files:

- `gradio_sms_text_classification.ipynb`: The main Jupyter notebook containing the Gradio application and SMS classification function.
- `sms_text_classification_solution.ipynb`: The notebook from which the SMS classification logic is derived.
- `SMSSpamCollection.csv`: The dataset used for training and testing the model.

## Before You Begin

1. **Create a New Repository**
   - Create a new repository named `sms_spam_detector`.
   - Do not add this homework assignment to an existing repository.

2. **Clone the Repository**
   - Clone the newly created repository to your local machine.

3. **Add Starter Files**
   - Download the starter files and place them inside your local Git repository.

4. **Push to GitHub or GitLab**
   - Commit your changes and push them to your remote repository.

## Challenge Instructions

### Step 1: Create the SMS Classification Function

In `gradio_sms_text_classification.ipynb`, implement the `sms_classification` function as follows:

1. **Set Features and Target Variables**
   - Set the `features` variable to the text message column of the DataFrame.
   - Set the `target` variable to the "label" column of the DataFrame.

2. **Data Splitting**
   - Split the data into training and testing sets with a `test_size` of 33%.

3. **Build and Fit the Model**
   - Build a pipeline to transform the test set to compare it with the training set.
   - Fit the model to the transformed training data and return the model.

4. **Load Data and Call Function**
   - Load `SMSSpamCollection.csv` into a DataFrame.
   - Call the `sms_classification` function with the DataFrame and assign the result to the `text_clf` variable.

### Step 2: Create the SMS Prediction Function

Implement the `sms_prediction` function to predict the classification of a new text:

1. **Prediction Variable**
   - Create a variable to hold the prediction of a new text.

2. **Conditional Statement**
   - Use a conditional statement to determine if the text message is "ham" or "spam".
   - Return a message indicating the classification:
     - For "ham": `f'The text message: "{text}", is not spam.'`
     - For "spam": `f'The text message: "{text}", is spam.'`

### Step 3: Create the Gradio Interface Application

1. **Gradio Interface**
   - Create a Gradio Interface application that takes a textbox for input and has a textbox for output.
   - Label the textboxes to describe their contents.

2. **Launch the Application**
   - Launch the application and provide the URL for sharing.

## Usage

1. Run the Jupyter notebook `gradio_sms_text_classification.ipynb`.
2. Input a text message in the provided textbox.
3. Click the submit button to receive feedback on whether the message is classified as spam or not.

## Example Output

When a user submits a message, they should see an output similar to the following:

- For a ham message:  
  *The text message: "Your appointment is confirmed.", is not spam.*

- For a spam message:  
  *The text message: "Congratulations! You've won a free gift card!", is spam.*
## Author 

Hoaward P. Dixon

- [Gradio](https://gradio.app/) for providing an easy-to-use interface for machine learning models.
- [Scikit-learn](https://scikit-learn.org/stable/) for the linear SVC implementation.


