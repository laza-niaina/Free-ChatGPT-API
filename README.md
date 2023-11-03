## Free ChatGPT API

### Introduction
This Free ChatGPT API allows you to use the text generation model interactively. You can use it to create chatbots, virtual assistants, or other text generation applications.

### Endpoint
The endpoint for this API is:
```
https://gpt-api-laza.onrender.com/v1/completions
```

### Request
The request must be of type `POST` and must include the following parameters:

1. `type`: This parameter specifies the type of conversation. In this example, the type is set to "chat".

2. `content`: This parameter corresponds to the content of the conversation. It must be an array of objects with the key-value pairs `from` and `content`. In this example, there is only one object with the values `from: "you"` and `content: "Hello, this is a test"`.

#### Example Request
```
curl -X POST -H "Content-Type: application/json" -d '{
    "type": "chat",
    "content": [
        {
            "from": "you",
            "content": "Hello, this is a test"
        }
    ]
}'https://gpt-api-laza.onrender.com/v1/completions
```

### Image Generation

To generate an image, you can pass the following parameters:

1. `type`: This parameter must be set to "image" to generate a specific image.

2. `content`: This parameter corresponds to the content of the conversation for image generation. It must be an object with the key-value pairs `from` and `content`. In this example, there is only one object with the values `from: "you"` and `content: "Elon musk"`.

3. `messages`: This parameter specifies the messages that accompany the image generation. In this example, the message is "Elon musk".

#### Example Request for Image Generation
```
curl -X POST -H "Content-Type: application/json" -d '{
    "type": "image",
    "content": [
        {
            "from": "you",
            "content": "Elon musk"
        }
    ],
    "messages": "Elon musk"
}'https://gpt-api-laza.onrender.com/v1/completions
```

### Response
The response from the API will be a JSON object

### Author
Email: <a href="mailto:lazaniaina13@gmail.com">Laza Niaina</a>
Facebook:  <a href="https://www.facebook.com/lazaniaina.r">Laza</a>
