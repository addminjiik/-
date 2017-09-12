WORK IN PROGRESS.

# CouchBot Commands

**In this section:**

- [Owner Commands](#owner-commands)
  - [Approved Admin Configuration](#approved-admin-configuration)
    - [`admin add [@DISCORD_USER_NAME]`](#add-approved-admin)
    - [`admin remove [@DISCORD_USER_NAME]`](#remove-approved-admin)
    - [`admin list`](#list-approved-admins)
  - [Channel Configuration](#channel-configuration)
    - [`channel live [#DISCORD_CHANNEL_NAME]`](#livestream-channel)
    - [`channel ownerlive [#DISCORD_CHANNEL_NAME]`](#owner-livestream-channel)
    - [`channel published [#DISCORD_CHANNEL_NAME]`](#published--vod-channel)
    - [`channel ownerpublished [#DISCORD_CHANNEL_NAME]`](#owner-published--vod-channel)
    - [`channel greetings [#DISCORD_CHANNEL_NAME]`](#greeting--goodbye-channel)
    - [`channel ownertwitchfeed [#DISCORD_CHANNEL_NAME]`](#owner-twitch-feed-channel)
    - [`channel clear [CHANNEL_TYPE]`](#clear-channel-settings)

## Owner Commands
### Approved Admin Configuration

An approved admin on your server will be able to add/remove streamers to/from the streamer lists. They WILL NOT be able to add/remove platform owner settings though.

#### Add Approved Admin

##### Command:

`admin add [@DISCORD_USER_NAME]`

##### Description:

Run this command to add a new approved admin to the server admin list.

##### Required Parameters

- `@DISCORD_USER_NAME` - This is the user you would like to add as an approved admin for your server. Note - You must TAG the user you'd like to add with the @ symbol followed by their username.

##### Example Usage:

`!cb admin add @dawgeth`

###### [Back to Top](#couchbot-commands)

------

#### Remove Approved Admin

##### Command:

`admin remove [@DISCORD_USER_NAME]`

##### Description:

Run this command to remove an approved admin from the server admin list.

##### Required Parameters

- `@DISCORD_USER_NAME` - This is the user you would like to remove as an approved admin for your server. Note - You must TAG the user you'd like to add with the @ symbol followed by their username.

##### Example Usage:

`!cb admin remove @dawgeth`

###### [Back to Top](#couchbot-commands)

------

#### List Approved Admins

##### Command:

`admin list`

##### Description:

Run this command to see a list of your servers approved admins.

##### Example Usage:

`!cb admin list`

###### [Back to Top](#couchbot-commands)

------

### Channel Configuration

Use the following commands to configure where the bot will send it's messages.

#### Livestream Channel

##### Command:

`channel live [#DISCORD_CHANNEL_NAME]`

##### Description:

Run this command to set the channel that livestream notifications will be sent to.

##### Required Parameters

- `#DISCORD_CHANNEL_NAME` - This is the channel you would like to send the notifications to. Note - Please tag the channel you'd like, starting with #.

##### Example Usage:

`!cb channel live #live-announcements`

###### [Back to Top](#couchbot-commands)

------

#### Owner Livestream Channel

##### Command:

`channel ownerlive [#DISCORD_CHANNEL_NAME]`

##### Description:

Run this command to set the channel that owner livestream notifications will be sent to.

##### Required Parameters

- `#DISCORD_CHANNEL_NAME` - This is the channel you would like to send the notifications to. Note - Please tag the channel you'd like, starting with #.

##### Example Usage:

`!cb channel ownerlive #live-announcements`

###### [Back to Top](#couchbot-commands)

------

#### Published / VOD Channel

##### Command:

`channel published [#DISCORD_CHANNEL_NAME]`

##### Description:

Run this command to set the channel that published notifications will be sent to.

##### Required Parameters

- `#DISCORD_CHANNEL_NAME` - This is the channel you would like to send the notifications to. Note - Please tag the channel you'd like, starting with #.

##### Example Usage:

`!cb channel published #new-videos`

###### [Back to Top](#couchbot-commands)

------

#### Owner Published / VOD Channel

##### Command:

`channel ownerpublished [#DISCORD_CHANNEL_NAME]`

##### Description:

Run this command to set the channel that owner published notifications will be sent to.

##### Required Parameters

- `#DISCORD_CHANNEL_NAME` - This is the channel you would like to send the notifications to. Note - Please tag the channel you'd like, starting with #.

##### Example Usage:

`!cb channel published #new-videos`

###### [Back to Top](#couchbot-commands)

------

#### Greeting / Goodbye Channel

##### Command:

`channel greetings [#DISCORD_CHANNEL_NAME]`

##### Description:

Run this command to set the channel that greeting and goodbye notifications will be sent to.

##### Required Parameters

- `#DISCORD_CHANNEL_NAME` - This is the channel you would like to send the notifications to. Note - Please tag the channel you'd like, starting with #.

##### Example Usage:

`!cb channel greetings #welcome-mat`

###### [Back to Top](#couchbot-commands)

------

#### Owner Twitch Feed Channel

##### Command:

`channel ownertwitchfeed [#DISCORD_CHANNEL_NAME]`

##### Description:

Run this command to set the channel that the owner Twitch feed notifications will be sent to.

##### Required Parameters

- `#DISCORD_CHANNEL_NAME` - This is the channel you would like to send the notifications to. Note - Please tag the channel you'd like, starting with #.

##### Example Usage:

`!cb channel ownertwitchfeed #twitch-feed`

###### [Back to Top](#couchbot-commands)

------

#### Clear Channel Settings

##### Command:

`channel clear [CHANNEL_TYPE]`

##### Description:

Run this command to clear the channel settings, whether it be a single setting, or all of them.

##### Required Parameters

- `#CHANNEL_TYPE` - This is the specific channel you'd like cleared. Your options are:

* live
* ownerlive
* published
* ownerpublished
* greetings
* ownertwitchfeed
* all

##### Example Usage:

`!cb channel clear live`

###### [Back to Top](#couchbot-commands)

------

---

#### "Allow" Configuration Options

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb allow mention true / false | Allow @ mentions at the start of your announcements. |
| !cb allow thumbnails true / false | Allow thumbnails in announcements. |
| !cb allow live true / false | Allow live content to be announced. |
| !cb allow published true / false | Allow published content to be announced. |
| !cb allow ownerchannelfeed true / false | Allw owner twitch channel feed announcements. |

---

#### Message Configuration Options

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb message live "YOUR MESSAGE HERE" | Set your own live message! Variables you can use: %CHANNEL%, %TITLE%, %URL%, and %GAME% (works Twitch, Mixer, and Smashcast. YouTube will put "a game" in place of the game title. API limitation :() |
| !cb message published "YOUR MESSAGE HERE" | Set your own Published Video message! Variables you can use: %CHANNEL%, %TITLE%, and %URL% |
| !cb message offline "YOUR MESSAGE HERE" | Set your own message to display when a stream goes offline (!cb config deleteoffline must be set to false) |
| !cb message testlive mixer / smashcast / twitch / youtube | Test the output of a specific platform. |
| !cb message testpublished | Test output of a published video. |

---

#### Greeting/Goodbye Configuration Options

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb greetings on /off | Toggle on or off greeting notifications. |
| !cb goodbyes on /off | Toggle on or off goodbyes notifications. |
| !cb greetings set "Your Welcome Message!" | Customize your greeting. %USER% and %NEWLINE% can be used to insert the newcomers name and/or a new line. |
| !cb goodbyes set "Your Goodbye Message!" | Customize your greeting. %USER% and %NEWLINE% can be used to insert the newcomers name and/or a new line. |

---

#### Misc. Configuration Options

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb config list | Check out your current configuration settings. |
| !cb config textannouncements true / false | Use old announcements if true, use embeds if false. |
| !cb config timezoneoffset NUMBER | Set your timezone offset from GMT. (ie: !cb config timezoneoffset |5 for EST) |
| !cb config deleteoffline true / false | If true, messages will be deleted when the user goes offline. If false, a message indicating it is now offline will be added. |
| !cb config mentionrole @ROLE|NAME | Set this to @everyone, or @YourCustomRole. This role will be announced if !cb allow mention is set to true. Please note | @here is not a valid role. This is unsusable. You can however, disable mentions .. and use @here in your custom messages. These commands can be found in the section right above this one :) |
| !cb config publishedytg true / false | www. vs gaming. on YouTube links. |

---

#### Test Commands

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb message testlive youtube / mixer / twitch / smashcast | Test live announcements. |
| !cb message testpublished | Test published announcements. |

---

### Owner (Manage Server Permissions) and Approved Admin Commands

---

#### Streamer Settings Configuration Options

NOTE: In the below commands, replace CHANNEL or CHANNELID with the name of your channel .. or channel id. 

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb streamer list | See a list of your configured streamers. |
| !cb mixer add channel | |
| !cb mixer remove channel | |
| !cb mixer owner channel | Can only have 1 owner per server. |
| !cb mixer resetowner | Reset the Owner Mixer channel.  |
| !cb picarto add Channel | |
| !cb picarto remove Channel | |
| !cb picarto owner Channel | |
| !cb picarto announce Channel | |
| !cb smashcast add channel | |
| !cb smashcast remove channel | |
| !cb smashcast owner channel | Can only have 1 owner per server.
| !cb smashcast resetowner | Reset the Owner Smashcast channel.  |
| !cb twitch add channel | |
| !cb twitch remove channel | |
| !cb twitch owner channel | Can only have 1 owner per server.
| !cb twitch resetowner | Reset the Owner Twitch channel. |
| !cb vidme add channelid | |
| !cb vidme remove channelid | |
| !cb vidme owner channelid | Can only have 1 owner per server. |
| !cb vidme resetowner | Reset the Owner Vidme channel. |
| !cb youtube add channelid | |
| !cb youtube remove channelid | |
| !cb youtube owner channelid | Can only have 1 owner per server. |
| !cb youtube resetowner | Reset the Owner YouTube channel. |

---

#### Game and Team Announcements (Twitch Only)

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb twitch addteam "teamtoken" |  ie: !cb twitch addteam "ths" for The Hammer Squad - To Add a Team |
| !cb twitch removeteam "teamtoken" |  ie: !cb twitch removeteam "ths" for The Hammer Squad - To Remove a Team |
| !cb twitch listteams | List teams you're monitoring. |
| !cb twitch addgame "Game Name" |  ie: !cb twitch addgame "League of Legends" - To Add a Game |
| !cb twitch removegame "Game Name" |  ie: !cb twitch removegame "League of Legends" - To Remove a Game |
| !cb twitch listgames | List gamesyou're monitoring. |

---

### Everyone! Commands
#### Bot Info Commands

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb invite | Get an invite link for CouchBot to join your server! |
| !cb uptime | See bot uptime. |
| !cb alerts | See the # of alerts that have been sent. |
| !cb info | # of Servers, Configured Users, and Helpful links. |

---

#### Misc. Commands

| Command Syntax | What It Does?! |
| -------------- | -------------- |
| !cb ytidlookup ChannelName | Need to lookup a YouTube Channel ID? Use this! (ie: !cb ytidlookup dawgeth) |
| !cb strawpoll create "QUESTION|CHOICE1,CHOICE2,etc|TRUE/FALSE for multi-choice" |
| !cb haibai | let folks know Hi! Then Bye! |