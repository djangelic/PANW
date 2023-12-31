### Integration Author: Angel Menendez
No support or maintenance is provided by the author. Customers are encouraged to engage with the user community for questions and guidance at the [Cortex XSOAR Live Discussions](https://live.paloaltonetworks.com/t5/cortex-xsoar-discussions/bd-p/Cortex_XSOAR_Discussions).
*****
CORTEX XSOAR Star Wars API (SWAPI) Integration
----------------------------------------------

This integration template/sample is meant to be used when building an integration that manages more than 1 kind of Incident Type.

If you plan on building an integration that handles only one incident type, then it will be easier to just use the createIncidents() class in Python instead as you can choose the incident type from the UI when adding your integration instance to the platform.

This integration also gives more control of the data routing to the SOC analysts, by making it visual and drag and droppable in the XSOAR Classifier editor. Consult with your local Jedi to see if the SWAPI integration is a good fit for you or your customer.  

This section explains how to configure the instance of the SWAPI Integration in Cortex XSOAR.

-   This integration does not require an API key and provides access to data about the Star Wars universe from the Star Wars API (SWAPI).
-   The integration includes commands to retrieve data about Star Wars films currently, and in the future will include indicators based on the characters, species, and starships.

*****

To configure the SWAPI integration on Cortex XSOAR:

1.  Navigate to Settings > Integrations > Servers & Services.
2.  Search for SWAPI.
3.  Click Add instance to create and configure a new integration instance.
4.  -   Name: a textual name for the integration instance.
    -   Fetch incidents: Whether the integration instance should fetch incidents. Checking this will cause the films to be brought into your instance.
    -   Incident type: If you have it, use your SWAPI incident type.
5.  Click Test to validate connection to the server.

Once the instance is successfully configured, you can run the commands from the Cortex XSOAR playground to get data about Star Wars characters, species, and starships.

The available commands are:

1.  fetch-incidents: Polls the SWAPI api for film data.
2.  swapi-fetch-films: Not yet active, but this will use the demisto create incidents class to create incidents directly from films
3.  test-module: Checks your network connection to ensure you have access to the api.

Please note that the SWAPI integration will only fetch incidents if you set the classifier and mapper.
