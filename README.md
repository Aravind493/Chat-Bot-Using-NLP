# Chat-Bot-Using-NLP

This project implements a simple chatbot using Python's NLTK library and Scikit-learn's TfidfVectorizer. The chatbot is capable of responding to user queries about chatbots using pre-existing text data. Let's break down the project into sections for better understanding:

1. Data Preprocessing:

    The project begins by reading text data from a file (chat.txt) and converting it to lowercase to ensure consistency in processing.
    NLTK is used to tokenize the text into sentences and words, which are essential for further processing.

2. Text Normalization:

    Text normalization is performed to preprocess the words in the text data. This includes lemmatization, which reduces words to their base or root form, and removing punctuation.

3. Greeting Function:

    A function greeting(sentence) is defined to detect if the user input contains greetings. If a greeting is detected, the chatbot responds with a random greeting from a 
    predefined list of responses.

4. Response Generation:

    The response(user_response) function generates a response to the user input based on the similarity between the input and pre-existing sentences in the dataset.
    It utilizes TF-IDF (Term Frequency-Inverse Document Frequency) vectorization to convert text data into numerical vectors and calculate cosine similarity between vectors to 
    measure their similarity.
    If the similarity score is above a certain threshold, the chatbot selects the most similar response from the dataset. Otherwise, it responds with a default message indicating 
    a lack of understanding.

5. User Interaction:

    The chatbot interacts with users through a console interface. It prompts the user to input queries and responds accordingly.
    If the user input contains a greeting, the chatbot responds with a greeting. Otherwise, it generates a response based on the user query using the response() function.
    The conversation continues until the user enters "bye," indicating the end of the interaction.

