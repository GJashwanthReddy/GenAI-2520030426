# LLM Provider Abstraction Using Python

The main objective of this experiment is to create a common interface for using different Large Language Model (LLM) providers.

The program supports both a cloud-based Gemini model and a locally running Ollama model. By using a common client, the application can send prompts without depending directly on one provider's implementation.

The experiment includes:

1. **`llm_client.py`** → Defines the common provider interface, Gemini and Ollama implementations, and the LLM client.
2. **`main.py`** → Runs the program and sends a prompt to the selected LLM provider.
3. **`test_client.py`** → Contains tests for the client functionality.
4. **`requirements.txt`** → Lists the required Python packages.
5. **`.env`** → Stores configuration such as the Gemini API key.

Install the required packages using:

**`python -m pip install -r requirements.txt`**

Gemini is accessed through the API, while Ollama can generate responses locally using the configured model.

In this experiment, the common client calls the provider to generate a response to the given prompt.
