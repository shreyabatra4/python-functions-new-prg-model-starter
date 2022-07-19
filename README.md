# New Programming Model for Azure Functions Python

## An easier way to create Functions using Python

The new programming model simplifies the Function App structure by having triggers and bindings represented as decorators, eliminating the need for the `function.json` configuration file, and creating an experience aligned with commonly used Python frameworks.

## Try it out

Documentation is avaiable here, examples for different extensions can found here, and view samples [here](https://github.com/Azure/azure-functions-python-worker/wiki).

## Callouts

- To define a trigger or binding, leverage intellisense by typing "trigger" or "output" to select templates. The previous experience of opening the command palette to add templates will not work.
- Mix and match of Functions written in the previous programming model and the new programming model in the same Function App will not be supported.
