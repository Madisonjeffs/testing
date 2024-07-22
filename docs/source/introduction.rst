Introduction
============

Overview
--------
The Steamworks Web API allows you to access various Steam features programmatically,
including player profiles, game news, and more.
We will be using it in order to enhance the customer's experience with the product via a companion app or website , by interlinking steam users 
with relative information.

Specific utilites of both the Web API and Steamworks API are clarified below:

Steamworks API Utilities
------------------------

The Steamworks API provides comprehensive features that are deeply integrated into the game client, enabling direct interaction with the Steam platform:

- **Tracking and Displaying Custom Achievements**: Manages and updates in-game achievements directly through Steam.
- **Recording and Displaying Player Statistics**: Integrates closely with games to track and update various in-game metrics.
- **Managing Global Leaderboards**: Handles the creation and updates of in-game leaderboards during competition seasons, including scores among friends.
- **Management of In-Game Microtransactions and DLC**: Oversees all in-game purchases, downloadable content, and inventory management via Steam.
- **Player Matchmaking**: Facilitates matchmaking services based on player skill levels or other criteria.
- **Management of Game Lobbies**: Supports dynamic matchmaking and manages game lobbies, enhancing the multiplayer experience.
- **Cloud Storage of User Saves**: Allows players to access their saved game data across various platforms through Steam Cloud.
- **Anti-Cheat Integration and Community Standards Management**: Implements anti-cheat measures and manages player behavior and bans within the community.


**It is important to note , that the Steamworks API and Steamworks Web API are separate. For internal integration with game engines see separate docs on Steamworks API**

For more detailed information on the Steamworks SDK API, please see the `official documentation <https://partner.steamgames.com/doc/sdk/api#1>`_.


Steam Web API Utilities
-----------------------

The Steam Web API is ideal for developers needing access to Steam data outside of the game environment, typically for integration with web or mobile applications:

- **Player Analytical Data**: Provides access to various analytical data about players, useful for third-party analysis and community-driven projects.



Audience
---------

This document is intended for internal use by our team at Scratch Demon Studios , to help them gain a quick and easy insight into  how to integrate the Steamworks web API for usage with our companion app / website.


Prerequisites
-------------

* To use this API you must have a steamworks account which can be obtained via the portal in the 'getting started' section.

* API keys , instructions to obtain these are included in the getting started section.

* An IDE set up , for standardised formatting Visual Studio Code will be the selection of choice.

* Python libraries for making HTTP requests, in this instance it can be done by importing the 'requests' library.

* Basic knowledge of REST APIs, JSON formatting and HTTP protocols.


