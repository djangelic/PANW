#### Integration Author: Angel Menendez

No support or maintenance is provided by the author. Customers are encouraged to engage with the user community for questions and guidance at the [Cortex XSOAR Live Discussions](https://live.paloaltonetworks.com/t5/cortex-xsoar-discussions/bd-p/Cortex_XSOAR_Discussions).
***
## CORTEX XSOAR Star Wars API (SWAPI) Integration
This section explains how to configure the instance of the SWAPI Integration in Cortex XSOAR.

- This integration does not require an API key and provides access to data about the Star Wars universe from the Star Wars API (SWAPI).
- The integration includes commands to retrieve data about Star Wars films currently, and in the future will include indicators based on the characters, species, and starships.

---
To configure the SWAPI integration on Cortex XSOAR:

1. Navigate to **Settings** > **Integrations** > **Servers & Services**.
2. Search for **SWAPI**.
3. Click **Add instance** to create and configure a new integration instance.
   - **Name**: a textual name for the integration instance.
   - **Fetch incidents**: Whether the integration instance should fetch incidents. Checking this will cause the films to be brought into your instance.
   - **Incident type**: If you have it, use your SWAPI incident type. 
4. Click **Test** to validate connection to the server.

Once the instance is successfully configured, you can run the commands from the Cortex XSOAR playground to get data about Star Wars characters, species, and starships.

The available commands are:

1. `get-character`: Retrieves details about a specific character.
2. `get-species`: Retrieves details about a specific species.
3. `get-starship`: Retrieves details about a specific starship.

Each command needs the relevant ID as an argument, e.g., `!get-character character_id=1` will retrieve information about the character with the ID 1.

Please note that the SWAPI integration does not support fetching incidents or indicators.

[View Integration Documentation](https://xsoar.pan.dev/docs/reference/integrations/swapi)
