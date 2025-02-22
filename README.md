# Ollama-API-Demo
This repository demonstrates two approaches to interact with the Ollama API for generating responses using the `deepseek-r1:1.5b` model. The examples showcase a manual HTTP request method and a Python client library method.

## Files in the Repository

### 1. `streaming_request.ipynb`
This file uses Python's `requests` library to directly send an HTTP POST request to the local Ollama API.  
- **Highlights**:
  - Handles a streaming response.
  - Manually parses the JSON response line-by-line.
  - Includes error handling for JSON decoding issues.

### 2. `ollama_client_example.ipynb`
This file uses the official `ollama` Python library to interact with the API.  
- **Highlights**:
  - Simplifies interaction with the API through a dedicated client library.
  - Directly prints the model's response without dealing with streaming or low-level request handling.

---

## Key Differences Between the Two Approaches

| Aspect                 | `streaming_request.py`                           | `ollama_client_example.py`                   |
|------------------------|--------------------------------------------------|----------------------------------------------|
| **Methodology**        | Uses raw HTTP requests (`requests` library).     | Utilizes the official `ollama` client.       |
| **Response Handling**  | Manually handles and streams the API response.   | Automatically manages response handling.     |
| **Complexity**         | More control but requires more boilerplate code. | Easier to implement with minimal setup.      |
| **Dependencies**       | Requires `requests` library.                     | Requires `ollama` library.                   |
| **Flexibility**        | Suitable for custom handling or streaming needs. | Ideal for straightforward API interactions.  |

---
