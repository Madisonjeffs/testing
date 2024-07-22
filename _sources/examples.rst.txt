Examples
========

Retrieving Player Summaries
----------------------------
To retrieve player summaries, send a `GET` request to the `/ISteamUser/GetPlayerSummaries/v2` endpoint:

.. code-block:: http

   GET /ISteamUser/GetPlayerSummaries/v2?steamids=76561198006409530,76561197960435530&key=YOUR_API_KEY HTTP/1.1
   Host: api.steampowered.com

Fetching News for an App
-------------------------
To fetch news for an app, send a `GET` request to the `/ISteamNews/GetNewsForApp/v2` endpoint:

.. code-block:: http

   GET /ISteamNews/GetNewsForApp/v2?appid=440&count=3&maxlength=300&key=YOUR_API_KEY HTTP/1.1
   Host: api.steampowered.com