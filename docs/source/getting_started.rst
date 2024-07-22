Getting Started
===================================
Base URL
--------
The base URL for the API is:

.. code-block:: text

   https://api.steampowered.com

Authentication
--------------
For some of the API methods, no authorization will be required. However for other methods with less publicly available data,
a unique API key may be required.
The methods that use customer sensitive data will require special access permissions and therefore require a publisher key.
The special publisher key will need to be created before calling such methods.

User Keys
-----------
Standard user keys are available to all, as long as a Steam account is held and the domain name associated with this key.

**The agreed terms of use for Steam Web API must be completed first** 

.. code-block:: text

   https://steamcommunity.com/dev/apiterms


Publisher Keys
--------------
To create a publisher API key, administrative access must be held within an existing steamworks account. 

To create a publisher key:

* Using the account with administrative access , visit the group list. This is done via Users & Permissions -> Manage Groups.

* From the list of groups , select or create a group that contains APP ID's for which access is desired with the WebAPI key.

* Click into that group to view users and apps within the group.

* The option to create a web API key should appear on the right hand side , or will be listed if already created.

Quick Start Guide
-----------------
This quick start guide will walk you through making your first API call to retrieve player summaries.

1. **Set Up Your Environment**:
   - Ensure you have Python installed.
   - Install the `requests` library using pip:

     .. code-block:: bash

        pip install requests

2. **Make Your First API Call**:
   - Use the following Python script to fetch player summaries:

     .. code-block:: python

        import requests

        # Your Steam Web API key
        api_key = 'YOUR_API_KEY'

        # Steam IDs of players to fetch
        steam_ids = '76561198006409530,76561197960435530'

        # Endpoint URL
        url = f'https://api.steampowered.com/ISteamUser/GetPlayerSummaries/v2?key={api_key}&steamids={steam_ids}'

        # Make the API request
        response = requests.get(url)

        # Check if the request was successful
        if response.status_code == 200:
            data = response.json()
            print("Player Summaries:", data)
        else:
            print("Error:", response.status_code, response.text)

3. **Analyze the Response**:
   - The response from the API will contain the player summaries for the specified Steam IDs. Here’s an example of the JSON response:

     .. code-block:: json

        {
            "response": {
                "players": [
                    {
                        "steamid": "76561198006409530",
                        "personaname": "Player1",
                        "profileurl": "http://steamcommunity.com/id/player1/",
                        "avatar": "http://media.steampowered.com/steamcommunity/public/images/avatars/xx/xx.jpg"
                    },
                    {
                        "steamid": "76561197960435530",
                        "personaname": "Player2",
                        "profileurl": "http://steamcommunity.com/id/player2/",
                        "avatar": "http://media.steampowered.com/steamcommunity/public/images/avatars/yy/yy.jpg"
                    }
                ]
            }
        }

Next Steps
----------
Now that you have successfully made your first API call, you can explore other Steamworks API features such as retrieving game stats, managing achievements, and more. Refer to the detailed endpoint documentation for further guidance.

For further assistance, please consult the Steamworks Developer documentation or contact the support team.

