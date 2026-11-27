# GOLDEN QUESTION SET AND LLM BASELINE EVALUATION – RELEASE v0.1

The main objective of this experiment is to evaluate a local Large Language Model (Llama 3.2 via Ollama) against a standardized golden question set of generative AI foundational concepts and establish a baseline performance benchmark (Release v0.1).

The program sends each question to the local Ollama API, evaluates the generated model response against domain keywords and expected answers, calculates a keyword coverage score, determines whether the response meets the passing threshold (score >= 60%), and logs detailed evaluation records to a CSV file.

The `golden_set.json` file is used to provide the 30 curated questions, reference sources, expected answers, and essential keywords. The `main.py` program loads these questions and runs the automated evaluation suite against the model.

Before running the code, ensure Ollama is installed and running with Llama 3.2 pulled (`ollama pull llama3.2`), activate the virtual environment, and install the required package using:

**`python -m pip install -r requirements.txt`**

Then run the program using:

**`python main.py`**

### The program:

1. Loads the 30 golden evaluation questions and expected keywords from `golden_set.json`.
2. Sends each prompt to the local Ollama LLM endpoint (`llama3.2`) with greedy decoding (temperature = 0).
3. Performs automated keyword matching between the model response and expected domain concepts.
4. Computes a keyword coverage score (percentage) and assigns a status (`PASS` if >= 60%, otherwise `REVIEW`).
5. Saves the detailed question-by-question evaluation logs to `baseline_results.csv`.
6. Prints a comprehensive baseline summary including total questions, pass/review counts, average keyword coverage, and officially labels the experiment as Release v0.1.

The program automatically creates:

**`baseline_results.csv`**
