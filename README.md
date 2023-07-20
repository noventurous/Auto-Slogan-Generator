# Auto-Slogan-Generator
AI Slogan Generator using Python and Text Transformers

# Installation
To run this script, you need to have Python 3 installed on your system. You also need to install the following libraries:

- nltk: Natural Language Toolkit for natural language processing
- wordnet: A lexical database for English
- text-gen: A text generation library based on GPT-2

You can install these libraries using pip:

pip install nltk
pip install wordnet
pip install text-gen

# Usage
To run this script, you need to have a slogan as an input. You can enter the slogan in the text input widget using streamlit.

To launch the streamlit app, run the following command in your terminal:

streamlit run slogan_generator.py

This will open a web browser and display the app. You can then enter your slogan in the input box and click the generate button to see the results.

The script will generate five new slogans based on your input using different transformations, such as synonym replacement, word order swapping, punctuation addition or removal, and word generation.

The results will be displayed on the app using streamlit.

# How it works
This script uses the following steps to generate new slogans from an existing one:

- Tokenize the slogan into words using nltk.word_tokenize
- Initialize an empty list to store the new slogans
- Loop over the number of new slogans to generate
  - Copy the original words list
  - Randomly choose a number of transformations to apply
  - Loop over the number of transformations
    - Randomly choose a type of transformation from ["synonym", "order", "punctuation", "generation"]
    - Apply the transformation according to the type
      - If synonym, randomly choose a word to replace with a synonym from wordnet.synsets
      - If order, randomly choose two words to swap their positions
      - If punctuation, randomly choose a word to add or remove punctuation
      - If generation, randomly choose a word to replace with a generated word using text-gen.text_generator
  - Join the new words into a new slogan and append it to the list
- Return the list of new slogans
Copy
Write a section on how to contribute to your code, including the license information, the coding standards, the testing methods, and the contact details. For example:
# Contribution
This script is licensed under the MIT License. You are free to use, modify, and distribute it as long as you give credit to the original author.

If you want to contribute to this script, you can follow these guidelines:

- Fork this repository on GitHub and clone it on your local machine.
- Create a new branch for your feature or bug fix.
- Write clean and consistent code that follows PEP 8 style guide for Python.
- Test your code using unittest or pytest frameworks.
- Commit your changes and push them to your forked repository.
- Create a pull request with a clear description of your changes.

  Enjoy!
