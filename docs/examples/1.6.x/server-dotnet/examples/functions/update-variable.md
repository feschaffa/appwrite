using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("<YOUR_PROJECT_ID>") // Your project ID
    .SetKey("<YOUR_API_KEY>"); // Your secret API key

Functions functions = new Functions(client);

Variable result = await functions.UpdateVariable(
    functionId: "<FUNCTION_ID>",
    variableId: "<VARIABLE_ID>",
    key: "<KEY>",
    value: "<VALUE>" // optional
);