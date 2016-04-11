#Overview
WoofBot is an edited version of [Airhorn Bot](https://airhorn.solutions/) for [Discord](https://www.discordapp.com/).

##Commands
Commands have been moved to the [wiki](https://github.com/Keshwoof/WoofBot/wiki/Commands).

##References
- [Discord API](https://discordapp.com/developers/docs/intro)
- [Go Language Documentation](https://golang.org/doc/)
- [DiscordGo Package](https://github.com/bwmarrin/discordgo)

#Installation / Running
(Instructions ~~shamelessly~~ shamefully taken & edited from the original repository.)

##Usage
WoofBot has two components, a bot client that handles the playing of audio, and a web server that implements OAuth2 and stats. Once added to your server, WoofBot can be summoned via the [many available commands](https://github.com/Keshwoof/WoofBot/wiki/Commands).

###Running the Bot
First install the bot: `go install github.com/Keshwoof/WoofBot`, then run the following command:

```
./airhornbot -r "localhost:6379" -t "MY_BOT_ACCOUNT_TOKEN" -o OWNER_ID
```

###Running the Web Server
First install the webserver: `go install github.com/Keshwoof/WoofBot`, then run `make static`, finally run:

```
./airhornweb -r "localhost:6379" -i MY_APPLICATION_ID -s 'MY_APPLICATION_SECRET"
```

Note, the webserver requires a redis instance to track statistics.

##Credits
|People|Cool stuff they did|
|---|---|
|[Hammer & Chisel](https://github.com/HammerAndChisel/)|Made Discord<br>Made Airhorn Bot|
|[iopred](https://github.com/iopred/)|Code reviewed Airhorn Bot<br>Works at Google|
|[bwmarrin](https://github.com/bwmarrin/)|Code reviewed Airhorn Bot<br>Made Go bindings for Discord|
