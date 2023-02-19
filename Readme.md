# Ensemble Chatbot API

This is a Flask app that provides an API for an ensemble chatbot that combines three pre-trained models to generate responses to user messages.

## Getting Started

To use the chatbot API, you can send a POST request to the `/api/chat` endpoint with a JSON payload that includes a `"message"` field with the user's message. The API will return a JSON response that includes a `"response"` field with the chatbot's generated response.

Here's an example using `curl`:

curl -X POST -H "Content-Type: application/json" -d '{"message": "Hello, how are you?"}' https://your-app-name.herokuapp.com/api/chat


The response will be in the following format:

{
"response": "Hello! I'm doing well, thank you. How can I assist you today?"
}


## Deploying to Heroku

To deploy the chatbot API to Heroku, follow these steps:

1. Create a new Heroku app.
2. Set the `FLASK_APP` environment variable to `app.py`.
3. Add the `gunicorn` and `transformers` Python packages to your `requirements.txt` file.
4. Push your code to Heroku.

## Acknowledgments

This chatbot API was created using pre-trained models from the following sources:

- [Hugging Face Transformers](https://huggingface.co/models)
- [TensorFlow Hub](https://tfhub.dev/s?q=dialogue)

Note: Replace "your-app-name" with the actual name of your app in the instructions above.

P.S: This is a free and open-source API. Feel free to use it in any of your projects.