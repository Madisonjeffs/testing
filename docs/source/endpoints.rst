Endpoints
=========

ISteamUser/GetPlayerSummaries
-----------------------------
Retrieve player summaries for a list of Steam IDs.

**HTTP Method:** `GET`

**Endpoint:**

.. code-block:: text

   /ISteamUser/GetPlayerSummaries/v2

**Parameters:**

* `steamids` (required): Comma-separated list of Steam IDs to fetch data for.
* `key` (required): Your Steam API key.

**Response:**

.. code-block:: json

   {
     "response": {
       "players": [
         {
           "steamid": "76561198006409530",
           "personaname": "Player1",
           "profileurl": "http://steamcommunity.com/id/player1/",
           "avatar": "http://media.steampowered.com/steamcommunity/public/images/avatars/xx/xx.jpg"
         }
       ]
     }
   }

ISteamNews/GetNewsForApp
------------------------
Retrieve news items for a specific app.

**HTTP Method:** `GET`

**Endpoint:**

.. code-block:: text

   /ISteamNews/GetNewsForApp/v2

**Parameters:**

* `appid` (required): The app ID to fetch news for.
* `count` (optional): Number of news items to retrieve (default is 20).
* `maxlength` (optional): Maximum length for news content (default is unlimited).
* `key` (required): Your Steam API key.

**Response:**

.. code-block:: json

   {
     "appnews": {
       "appid": 440,
       "newsitems": [
         {
           "gid": "123456",
           "title": "Update Released",
           "url": "http://store.steampowered.com/news/123456/",
           "is_external_url": false,
           "author": "Valve",
           "contents": "An update has been released.",
           "feedlabel": "Valve",
           "date": 1625217600,
           "feedname": "steam_updates",
           "feed_type": 0,
           "appid": 440
         }
       ]
     }
   }


ISteamUserStats/GetPlayerAchievements
-------------------------------------
Retrieve a list of achievements completed by a user for a specific game.

**HTTP Method:** `GET`

**Endpoint:**

.. code-block:: text

   /ISteamUserStats/GetPlayerAchievements/v1

**Parameters:**

* `steamid` (required): Steam ID of the user.
* `appid` (required): The application ID of the game.
* `key` (required): Your Steam API key.
* `l` (optional): Language for the response (e.g., "en" for English).

**Response:**

.. code-block:: json

   {
     "playerstats": {
       "steamID": "76561198006409530",
       "gameName": "Game Name",
       "achievements": [
         {
           "apiname": "ACH_WIN_ONE_GAME",
           "achieved": 1,
           "unlocktime": 1588364923
         },
         {
           "apiname": "ACH_WIN_TWO_GAMES",
           "achieved": 0,
           "unlocktime": 0
         }
       ],
       "success": true
     }
   }

ISteamUserStats/GetUserStatsForGame
------------------------------------
Retrieve user statistics for a specific game.

**HTTP Method:** `GET`

**Endpoint:**

.. code-block:: text

   /ISteamUserStats/GetUserStatsForGame/v2

**Parameters:**

* `steamid` (required): Steam ID of the user.
* `appid` (required): The application ID of the game.
* `key` (required): Your Steam API key.

**Response:**

.. code-block:: json

   {
     "playerstats": {
       "steamID": "76561198006409530",
       "gameName": "Game Name",
       "stats": [
         {
           "name": "total_kills",
           "value": 3407
         },
         {
           "name": "total_deaths",
           "value": 1278
         }
       ],
       "success": true
     }
   }

ISteamGameServer/GetServerInfo
-------------------------------
Retrieve information about a game server.

**HTTP Method:** `GET`

**Endpoint:**

.. code-block:: text

   /ISteamGameServer/GetServerInfo/v1

**Parameters:**

* `serverids` (required): Comma-separated list of server IDs.
* `key` (required): Your Steam API key.

**Response:**

.. code-block:: json

   {
     "servers": [
       {
         "serverid": "90071996842377217",
         "name": "Server Name",
         "appID": 440,
         "gameDir": "tf",
         "version": "1.0.0.0",
         "addr": "192.168.1.1:27015"
       }
     ]
   }