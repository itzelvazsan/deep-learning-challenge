# deep-learning-challenge

By: Itzel Vázquez Sánchez

## Project Description
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received access to a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

This Project is the result of the learning lessons of Module 21: Deep Learning from the Data Analysis and Visualization Boot Camp 2025. The main goal is to use the acquired habilities and knowledge in a real case. 

### Step 1. Preprocess the Data

Start by uploading the starter file to Google Colab, then using the information we provided in the Challenge files, follow the instructions to complete the preprocessing steps.

1. From the provided cloud URL, read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:

Target variable: IS_SUCCESSFUL
Feature(s): APPLICATION_TYPE—Alphabet Soup application type; AFFILIATION—Affiliated sector of industry; CLASSIFICATION—Government; organization classification; USE_CASE—Use case for funding; ORGANIZATION—Organization type; STATUS—Active status; INCOME_AMT—Income classification; SPECIAL_CONSIDERATIONS—Special considerations for application; ASK_AMT—Funding amount requested

2. Drop the EIN and NAME columns.
3. Determine the number of unique values for each column.
4. For columns that have more than 10 unique values, determine the number of data points for each unique value.
5. Use the number of data points for each unique value to pick a cutoff point to combine "rare" categorical variables together in a new value, Other, and then check if the replacement was successful.
6. Use pd.get_dummies() to encode categorical variables.
7. Split the preprocessed data into a features array, X, and a target array, y. Use these arrays and the train_test_split function to split the data into training and testing datasets.
8. Scale the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.

### Step 2. Compile, Train, and Evaluate the Model
1. Continue using the file in Google Colab in which you performed the preprocessing steps from Step 1.
2. Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.
3. Create the first hidden layer and choose an appropriate activation function.
4. If necessary, add a second hidden layer with an appropriate activation function.
5. Create an output layer with an appropriate activation function.
6. Check the structure of the model.
7. Compile and train the model.
8. Create a callback that saves the model's weights every five epochs.
9. Evaluate the model using the test data to determine the loss and accuracy.
10. Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity.h5

### Step 3. Optimize the Model
1. Create a new Google Colab file and name it AlphabetSoupCharity_Optimization.ipynb.
2. Import your dependencies and read in the charity_data.csv to a Pandas DataFrame from the provided cloud URL.
3. Preprocess the dataset as you did in Step 1. Be sure to adjust for any modifications that came out of optimizing the model.
4. Design a neural network model, and be sure to adjust for modifications that will optimize the model to achieve higher than 75% accuracy.
5. Save and export your results to an HDF5 file. Name the file AlphabetSoupCharity_Optimization.h5.

### Step 4. Write a Report on the Neural Network Model

The report should contain the following:
1. Overview of the analysis: Explain the purpose of this analysis.
2. Results: Address the following questions: What variable(s) are the target(s) for your model? // What variable(s) are the features for your model? // What variable(s) should be removed from the input data because they are neither targets nor features? //
3. Compiling, Training, and Evaluating the Model:  How many neurons, layers, and activation functions did you select for your neural network model, and why? // Were you able to achieve the target model performance? // What steps did you take in your attempts to increase model performance?
4. Summary: Summarize the overall results of the deep learning model

### Step 5. Copy Files Into Your Repository
1. Download your Colab notebooks to your computer.
2. Move them into your Deep Learning Challenge directory in your local repository.
3. Push the added files to GitHub.

n the repository you can find the following content:

| Item  |   File Type   |         File Name                |           Description                   |
| ----- | ------------- | ---------------------------------| --------------------------------------- |
|   1   |     folder    |   Deep_Learning_Challenge        |contains 2 ipynb with challenge's answers|
| 1.1   |    .ipynb     |  AlphabetSoupCharity             |First and second parts of the challenge  |
| 2.2   |    .ipynb     | AlphabetSoupCharity_Optimization |    Third part of the challenge          |
|   2   |     md        |           Report                 | Fourth part of the challenge

## How to Use the Project
* Download the repository and upload it into Google Drive. Run the AlphabetSoupCharity.ipynb and analyze the results. After that, un the AlphabetSoupCharity_Optimization.ipynb and compare the results.

## Credits 

The code of this project origins from: starter code provided by the Team of the Data Analysis and Visualization Bootcamp, the solved exercises worked in the Zoom Lessons, [Stackoverflow](https://stackoverflow.com/), [pandas documentation](https://pandas.pydata.org/docs/index.html), and Microsoft Copilot.
