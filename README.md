# Chatbot Readme

## Description

This chatbot is designed to engage in conversation with users, providing responses based on predefined patterns and intent data. The chatbot utilizes a neural network model trained on various intent datasets, including general intents, health-related intents, and booking-related intents. The model employs fuzzy string matching to determine the best response to user input.

## Required Libraries

- `requests`
- `json`
- `numpy`
- `tensorflow`
- `sklearn`
- `fuzzywuzzy`
- `colorama`

## Import Libraries

The code begins by importing the necessary libraries and modules, including TensorFlow for the neural network, scikit-learn for label encoding, fuzzywuzzy for string matching, and colorama for terminal colors.

## Load Intent Data

Intent data is loaded from multiple JSON files, each containing a set of predefined intents and patterns for the chatbot to recognize and respond to.

## Chatbot Function (`chat()`)

The chatbot function is the core of the interaction with users. It performs the following steps:

### Model Loading

- Loads a pre-trained neural network model (`chat_model`) using TensorFlow Keras.

### Tokenizer and Label Encoder Loading

- Loads the tokenizer and label encoder objects from their respective pickle files, which were saved during the training phase.

### User Interaction Loop

- Initiates a while loop for continuous interaction with the user until the user inputs 'quit'.

### User Input Processing

- Takes user input and processes it for further analysis.

### Intent Matching with Fuzzy String Matching

- Utilizes fuzzy string matching (fuzzywuzzy) to compare user input with patterns in each set of intents.
- Determines the best response based on the highest similarity score for each set of intents.

### Response Generation

- Provides responses based on the best similarity score found.
- If the similarity score is above a certain threshold (70), and a suitable response is found, the chatbot displays the response.
- If the similarity score is below the threshold or no suitable response is found, it displays a default response indicating an error in the user input.

## Main Block

The main block of code includes the necessary imports, intent data loading, and the invocation of the `chat()` function to start the chatbot. It also allows the user to exit the chat by typing 'quit'.

## Usage

1. Ensure that all required libraries are installed using the specified versions.
2. Run the code to start the chatbot.
3. Interact with the chatbot by typing messages.
4. Type 'quit' to exit the chatbot.

Feel free to customize the code, add more intents, or enhance the model for specific use cases.
