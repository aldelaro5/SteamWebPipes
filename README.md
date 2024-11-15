# About this fork

* Using SQLite database instead of MySQL
* Add an DBUpdater written in Go, to update local SQLite database
* Change realtime.js, let the links point to SteamDB.info

This fork aids to let it run on a personal computer without any extra setups.

# SteamWebPipes

Uses Steam's PICS changelist system and retransmits it to clients via WebSockets.

This is a barebones program which uses SteamKit2 library. All it does is check for new changelists,
and when detected sends out events to Websocket clients.

If a MySQL database string is provided, it will pull app and package names from there.
See `ChangelistEvent.cs` file and modify as needed. You can seed app names by using GetAppList web API.

It requires .NET 9. The client (in `client/` folder) connects to the Websocket and prints the
events as they are received.

License: [MIT](LICENSE)
