# Threema Broadcast Integration for Shuffler.io

This integration enables interaction with the **Threema Broadcast API**, allowing you to automate and manage broadcast messaging, retrieve chat histories, interact with distribution lists and perform other broadcast-related operations directly within Shuffler.io.

The API available is well documented in the Threema Broadcast API Official Documentation: https://broadcast.threema.ch/en/api-doc

## Prerequisites

Before using this project, you will need:

- A Threema Broadcast account with the necessary API credentials.
- A Threema Broadcast distribution list with the desired recipients assigned to it.

To get the API key neccessary for this connector, go to `Settings` at the top bar. Select your user and `API keys` afterwards. Click on `Create API key` twice and copy your API key you just created.

## Configuration

To configure the Threema Broadcast app in Shuffler.io, follow these steps:

1. **API Key**: 
   - Obtain your API key from the Threema Broadcast console.
   - Enter it in the `Apikey` field securely.

2. **Broadcast UID** (when needed):
   - Provide the unique identifier (`BroadcastUid`) of the broadcast you wish to interact with.
   - The UID is not the same as the ID (it is not the one that starts with a "*").
   - To get this value, you need to execute a GET request with the Threema Broadcast API to /identities, which could be also performed in your workflow.

3. **Distribution List UID, Group Chat UID, etc.** (when needed):
   - Provide the unique identifier of the Distribution List, Chat Group... you wish to interact with.
   - To get this value, you need to execute the corresponding GET request with the Threema Broadcast API, which could be also performed in your workflow.


## Headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

These headers ensure proper communication with the Threema API.

## Example Usage

### Retrieve Group Chat History
1. Set up the action **Get group chat history**.
2. Fill in the following fields:
   - **Apikey**: Enter your API key.
   - **Url**: `https://broadcast.threema.ch`.
   - **GroupUid**: Provide the group UID.

3. Execute the action to retrieve the chat history for the specified group.

## Notes

- For detailed API documentation, visit the Threema Broadcast API Official Documentation: https://broadcast.threema.ch/en/api-doc.

## Support

If you encounter issues, refer to the Threema API documentation or contact your Shuffler.io administrator.
