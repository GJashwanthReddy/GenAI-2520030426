# LLM Usage Monitoring and Logging

The main objective of this experiment is to monitor LLM usage and record information about requests and responses.

The program uses a client to make LLM calls and a logging component to keep track of usage details. This helps observe the requests made to the model and review usage information after execution.

The experiment includes the following Python files:

1. **`main.py`** → Runs the program and makes the LLM request.
2. **`llm_client.py`** → Handles the LLM provider and client functionality.
3. **`usage_logger.py`** → Records usage-related information during LLM calls.
4. **`test_client.py`** → Contains tests for the client.
5. **`requirements.txt`** → Lists the required packages.

Install the required packages using:

**`python -m pip install -r requirements.txt`**

Run the main program to send a prompt and record the associated usage information through the logger.
