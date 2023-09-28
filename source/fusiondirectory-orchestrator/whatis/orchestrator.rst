What is FusionDirectory Orchestrator ?
======================================

| FusionDirectory Orchestrator provides a web service solution serving a REST API.
| It allows a granular management of some specialized tasks.

Features
^^^^^^^^

- Tasks management.
- Tasks execution.
- JWT Authentication methods


Tasks management
^^^^^^^^^^^^^^^^

| FusionDirectory Orchestrator REST API allows the retrieval of existing created Tasks.  
| Offering a simple view on the status of each tasks. 

It is possible to retrieve specialized tasks such as Mail. 

Tasks execution
^^^^^^^^^^^^^^^

| One of the main aspect of FusionDirectory Orchestrator is to allow processing of some desired tasks.
| In case of a task of type mail, the list of related emails will be sent if scheduled is matched.

JWT authentication
^^^^^^^^^^^^^^^^^^

| It was decided to enhance our authentication mechanism and use the JWT methodology.
| Allowing after proper username/password authentication the reception of an access and refresh token.

The access token is to be used for any operations on FusionDirectory Orchestrator endpoints. 


