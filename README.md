# Sample AI Foundry API Client

This is a sample API built using FastAPI that showcases how to establish an authenticated session to Azure AI Foundry as the end-user. This is useful when using AI Foundry's built-in knowledge tools such as Fabric and Databricks integration, which both implement the on-behalf-of flow to ensure data is fetched using the security context of the user making the call.

## Local Environment Setup

Ensure you have the following installed in your local environment:

* [Python Language Support for VS Code](https://marketplace.visualstudio.com/items/?itemName=ms-python.python) extension installed and running.

* The most recent version of [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli) is installed and working.

This repo assumes an environment running Ubuntu 24 LTS running on Windows 11 via Windows Subsystem for Linux with Python 3.12 or higher installed:

```bash
sudo apt install python
sudo apt install python3-pip
sudo apt install python-is-python3
sudo apt install python3.12-venv
```

Next, create a Python virtual environment at the root project folder:

```bash
python -m venv .venv
source .venv/bin/activate
```

Next, use the `requirements.txt` file to install the Python packages:

```bash
pip install -r requirements.txt
```

## App Configuration

Create a `.env` file under the **src** directory and use the provided [env.example](/src/env.example) file to add the necessary environment variables. Be sure to update each value to match your environment.

## Run and Debug

This repo includes a configuration for running and debugging the API. Simply select the "FastAPI" configuration in the "Run and Debug" pane.

## Run the Application

This demo API was written using [FastAPI](https://github.com/FastAPI/FastAPI). Use the following command to run it without the debugger:

```bash
fastapi dev src/main.py
```
