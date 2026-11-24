# TOKEN ECONOMICS – FEATURE BUDGET CALCULATOR

The main objective of this experiment is to estimate the token usage and cost of an AI feature before building or deploying it.

The program calculates the expected input and output tokens per day, estimated daily and monthly API costs, and peak requests and tokens per minute. It also checks the usage against RPM and TPM limits and the configured daily and monthly budgets.

The `.env` file is used to provide the usage assumptions, token pricing, rate limits, budgets, and safety margin. The `budget.py` program loads these values and calculates a report.

Before running the code, activate the virtual environment and install the required package using:

**`python -m pip install -r requirements.txt`**

Then run the program using:

**`python budget.py`**

### The program:

1. Loads the configuration values from `.env`.
2. Calculates daily input, output, and total token usage.
3. Estimates daily and monthly costs.
4. Calculates peak RPM and TPM with a safety margin.
5. Checks rate limits and budgets, and prints a recommendation.

To test the calculations, run:

**`python -m unittest test_budget.py`**
