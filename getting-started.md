# Getting Started with Azure Functions in Python (New Programming Model)
  

## New Programming Model (Preview)

The new programming model in Azure Functions Python delivers an experience that aligns with Python development principles, and subsequently with commonly used Python frameworks. 

The improved programming model requires fewer files than the default model, and specifically eliminates the need for a configuration file (`function.json`). Instead, triggers and bindings are represented in the `function_app.py` file as decorators. Moreover, functions can be logically organized with support for multiple functions to be stored in the same file. Functions within the same function application can also be stored in different files, and be referenced as blueprints.

In addition to the [published documentation](<TODO>), hints are available in code editors that support type checking with PYI files.

## Notes

- Mix and match of Functions written in the previous programming model and the new programming model in the same Function App will not be supported.
- At this time, the main functions file must be named `function_app.py`.

To learn more about the new programming model for Azure Functions in Python, see the [Azure Functions Python developer guide](https://docs.microsoft.com/en-us/azure/azure-functions/functions-reference-python?tabs=asgi%2Capplication-level).

## Getting Started

Project Structure

The main project folder (<project_root>) can contain the following files:

* *function_app.py*: Functions along with their triggers and bindings are defined here.
* *local.settings.json*: Used to store app settings and connection strings when running locally. This file doesn't get published to Azure. To learn more, see [local.settings.file](functions-develop-local.md#local-settings-file).
* *requirements.txt*: Contains the list of Python packages the system installs when publishing to Azure.
* *host.json*: Contains configuration options that affect all functions in a function app instance. This file does get published to Azure. Not all options are supported when running locally. To learn more, see [host.json](functions-host-json.md).
* *additional_functions.py*: (Optional) Functions that are defined in a separate file for logical organization and grouping, that can be referenced in `function_app.py`.    
* *.vscode/*: (Optional) Contains store VSCode configuration. To learn more, see [VSCode setting](https://code.visualstudio.com/docs/getstarted/settings).
* *.venv/*: (Optional) Contains a Python virtual environment used by local development.
* *Dockerfile*: (Optional) Used when publishing your project in a [custom container](functions-create-function-linux-custom-image.md).
* *tests/*: (Optional) Contains the test cases of your function app.
* *.funcignore*: (Optional) Declares files that shouldn't get published to Azure. Usually, this file contains `.vscode/` to ignore your editor setting, `.venv/` to ignore local Python virtual environment, `tests/` to ignore test cases, and `local.settings.json` to prevent local app settings being published.
  
## Developing your first Python function using VS Code

If you have not already, please checkout our quickstart to get you started with Azure Functions developments in Python.

Publishing your function app to Azure
  
For more information on deployment options for Azure Functions, please visit this guide.

## Next Steps
  
To learn more about developing Azure Functions, please visit Azure Functions Developer Guide.

To learn more specific guidance on developing Azure Functions with Python, please visit Azure Functions Developer Python Guide.
