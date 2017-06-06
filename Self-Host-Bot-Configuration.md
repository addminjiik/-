Migrating to a New Version? (This Migration)[https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Migration] document may help!

1. Go to [https://console.developers.google.com](https://console.developers.google.com). Create an app. Create API key. Save that API Key.
2. Go to [https://www.twitch.tv/settings/connections](https://www.twitch.tv/settings/connections). Click Register your application. Create a new application. Save your Client ID.
3. Go to [https://discordapp.com/developers/applications](https://discordapp.com/developers/applications). Click New App. Name the app what you want the bot to be named. Set the Icon to the Avatar you want to use. Create a new app. Click Create a Bot User. Save the Client ID and the Token (click reveal in the Bot User section).
4. Go to the CouchBotRelease folder created during the [installation process](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation). 
5. Edit BotSettings.json with your favorite text editor. [I really like Notepad++](https://notepad-plus-plus.org/).
6. Replace the following values with your keys created in steps 1-3.

```json
  "Keys": {  
    "DiscordToken": "DISCORDTOKEN",  
    "TwitchClientId": "TWITCHID",  
    "YouTubeApiKey": "YOUTUBEAPI"  
  }  
```

7. Replace the following values with your Discord Client Id and a Prefix you want to use (ie: !cb). You won't need TotalShards unless your bot joins over 2500 servers.

```json
  "BotConfiguration": {
    "CouchBotId": 0,
    "Prefix": "",
    "TotalShards":  1
  }
```

8. This section allows for customizing paths to folders. Make sure you use \\ instead of \, and this is where Linux and Mac users can customize their pathing.

```json
  "Directories": {
    "ConfigRootDirectory": "C:\\programdata\\CouchBot\\",
    "GuildDirectory": "Guilds\\",
    "UserDirectory": "Users\\",
    "LiveDirectory": "Live\\",
    "MixerDirectory": "Mixer\\",
    "PicartoDirectory": "Picarto\\",
    "SmashcastDirectory": "Smashcast\\",
    "TwitchDirectory": "Twitch\\",
    "YouTubeDirectory": "YouTube\\"
  }
```

9. Want to enable/disable a platform? This section is for you. VidMe is partially implemented and not functioning as of 6/6/2017.

```json
  "Platforms": {
    "EnableMixer": true,
    "EnableSmashcast": true,
    "EnableTwitch": true,
    "EnableYouTube": true,
    "EnablePicarto": true,
    "EnableVidMe":  true
  }
```

10. If you want to change how many seconds between checks your bot waits - modify the values here. Please note, YouTube will churn and burn your quota. Be careful how low you set it, and the other platforms.

```json
  "Intervals": {
    "Picarto": 120,
    "Smashcast": 120,
    "Twitch": 300,
    "TwitchFeed": 300,
    "YouTubePublished": 900,
    "YouTubeLive": 300,
    "VidMe":  900
  }
```

Have any feedback? See anything I missed? Please open and issue above and let me know!