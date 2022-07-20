# Blob Trigger - Python (New Programming Model)

## Blob Trigger

The Blob storage trigger starts a function when a new or updated blob is detected. The blob contents are provided as input to the function. The Azure Blob storage trigger requires a general-purpose storage account. Storage V2 accounts with hierarchical namespaces are also supported.

## Using the Template

Blob Trigger code snippet

```python
import logging

import azure.functions as func

app = func.FunctionApp()

@app.function_name(name="BlobTrigger1")
@app.blob_trigger(arg_name="myblob", path="samples-workitems/{name}",
                  connection="")
def test_function(myblob: func.InputStream):
   logging.info(f"Python blob trigger function processed blob \n"
                f"Name: {myblob.name}\n"
                f"Blob Size: {myblob.length} bytes")
```

To run the code snippet generated through the command palette, note the following:

- The function application is defined and named `app`.
- Confirm that the parameters within the trigger reflect values that correspond with your storage account.

To learn more about using the Blob Trigger in the new Python programming model for Azure Functions, see <TODO>.

- It is assumed the name of the function application is `app`. If this is not the name of your function application, please rename it in the sample code accordingly.

## New Programming Model (Preview)

The new programming model in Azure Functions Python delivers an experience that aligns with Python development principles, and subsequently with commonly used Python frameworks. 

The improved programming model requires fewer files than the default model, and specifically eliminates the need for a configuration file (`function.json`). Instead, triggers and bindings are represented in the `function_app.py` file as decorators. Moreover, functions can be logically organized with support for multiple functions to be stored in the same file. Functions within the same function application can also be stored in different files, and be referenced as blueprints.

In addition to the [published documentation](<TODO>), hints are available in code editors that support type checking with PYI files.

To learn more about the new programming model for Azure Functions in Python, see <TODO>.

