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
  - [Allow Configuration](#allow-configuration)
    - [`allow mention [true / false]`](#mention-role)
    - [`allow thumbnails [true / false]`](#thumbnails)
    - [`allow live [true / false]`](#live)
    - [`allow published [true / false]`](#published-vod)
    - [`allow ownerchannelfeed [true / false]`](#twitch-owner-channel-feed)
  - [Message Configuration](#message-configuration)
    - [`message live "[Your Custom Message]"`](#live-message)
	- [`message published "[Your Custom Message]"`](#published-message)
	- [`message offline "[Your Custom Message]"`](#offline-message)
	- [`message testlive [PLATFORM]`](#test-live-message)
	- [`message testpublished`](#test-published-message)
  - [Greeting / Goodbye Configuration](#greeting--goodbye-configuration)
    - [`greetings [on / off]`](#greetings)
	- [`goodbyes [on / off]`](#goodbyes)
	- [`greetings set "[Your Custom Message]"`](#greeting-message)
	- [`goodbyes set "[Your Custom Message]"`](#goodbye-message)


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

`!cb channel ownerpublished #new-videos`

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

### Allow Configuration

Use the following commands to configure what the bot is allowed to do.

#### Mention Role

##### Command:

`allow mention [true / false]`

##### Description:

Run this command to allow / deny the ability for announcements to contain an @role announcement.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb allow mention true`

###### [Back to Top](#couchbot-commands)

------

#### Thumbnails

##### Command:

`allow thumbnails [true / false]`

##### Description:

Run this command to allow / deny the ability for announcements to contain a thumbnail.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb allow thumbnails true`

###### [Back to Top](#couchbot-commands)

------

#### Live

##### Command:

`allow live [true / false]`

##### Description:

Run this command to allow / deny the ability for livestream announcements.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb allow live true`

###### [Back to Top](#couchbot-commands)

------

#### Published / VOD

##### Command:

`allow published [true / false]`

##### Description:

Run this command to allow / deny the ability for published / VOD announcements.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb allow published true`

###### [Back to Top](#couchbot-commands)

------

#### Twitch Owner Channel Feed

##### Command:

`allow ownerchannelfeed [true / false]`

##### Description:

Run this command to allow / deny the ability for Twitch Owner channel feed announcements.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb allow ownerchannelfeed true`

###### [Back to Top](#couchbot-commands)

------

### Message Configuration

Use the following commands to configure custom message options and test them.

#### Live Message

##### Command:

`message live "[Your Custom Message]"`

##### Description:

Run this command to set a custom message to be announced when configured channels go live.

##### Required Parameters

- `Your Custom Message` - This message has to be surrounded with quotes. You can include the following custom variables... %CHANNEL%, %TITLE%, %URL%, and %GAME%. Note, %GAME% doesn't work on YouTube. It will be replaced with "a game".

##### Example Usage:

`!cb message live "%CHANNEL% just went live - %TITLE% - Playing %GAME% - Click to Watch: %URL%"`

###### [Back to Top](#couchbot-commands)

------

#### Published Message

##### Command:

`message published "[Your Custom Message]"`

##### Description:

Run this command to set a custom message to be announced when configured channels publish new content.

##### Required Parameters

- `Your Custom Message` - This message has to be surrounded with quotes. You can include the following custom variables... %CHANNEL%, %TITLE%, and %URL%.

##### Example Usage:

`!cb message published "%CHANNEL% just posted a new video - %TITLE% - Click to Watch: %URL%"`

###### [Back to Top](#couchbot-commands)

------

#### Offline Message

##### Command:

`message offline "[Your Custom Message]"`

##### Description:

Run this command to replace the default Stream Offline message that displays when a streamer goes offline. (Please note - only used if !cb config deleteoffline is set to false.)

##### Required Parameters

- `Your Custom Message` - This message has to be surrounded with quotes.

##### Example Usage:

`!cb message offline "This stream is now offline. Sorry you missed the fun."`

###### [Back to Top](#couchbot-commands)

------

#### Test Live Message

##### Command:

`message testlive [PLATFORM]`

##### Description:

Run this command to test your custom live message. This will display in your current channel, not the live channel you have set.

##### Required Parameters

- `[PLATFORM]` - Replace with: mixer, smashcast, twitch, or youtube.

##### Example Usage:

`!cb message testlive mixer`

###### [Back to Top](#couchbot-commands)

------

#### Test Published Message

##### Command:

`message testpublished`

##### Description:

Run this command to test your custom published message. This will display in your current channel, not the live channel you have set.

##### Example Usage:

`!cb message testpublished`

###### [Back to Top](#couchbot-commands)

------

### Greeting / Goodbye Configuration

Use the following commands to configure greeting and goodbye functionality.

#### Greetings

##### Command:

`greetings [on / off]`

##### Description:

Run this command to turn greetings on / off.

##### Required Parameters

- `on / off` - On for on. Off for off.

##### Example Usage:

`!cb greetings on`

###### [Back to Top](#couchbot-commands)

------

#### Goodbyes

##### Command:

`goodbyes [on / off]"`

##### Description:

Run this command to turn goodbyes on / off.

##### Required Parameters

- `on / off` - On for on. Off for off.

##### Example Usage:

`!cb goodbyes off`

###### [Back to Top](#couchbot-commands)

------

#### Greeting Message

##### Command:

`greetings set "[Your Custom Message]"`

##### Description:

Run this command to replace the default Greeting message.

##### Required Parameters

- `Your Custom Message` - This message has to be surrounded with quotes. Use the variables %USER% to dynamically insert the new users name, or %NEWLINE% for a line break.

##### Example Usage:

`!cb greetings set "Hello there, %USER%!"`

###### [Back to Top](#couchbot-commands)

------

#### Goodbye Message

##### Command:

`goodbyes set "[Your Custom Message]"`

##### Description:

Run this command to replace the default Goodbye message.

##### Required Parameters

- `Your Custom Message` - This message has to be surrounded with quotes. Use the variables %USER% to dynamically insert the new users name, or %NEWLINE% for a line break.

##### Example Usage:

`!cb goodbyes set "Good bye, %USER%!"`

###### [Back to Top](#couchbot-commands)

------




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