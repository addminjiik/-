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
    - [`allow published [true / false]`](#published--vod)
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
	- [`greetings test`](#test-greeting-message)
	- [`goodbyes test`](#test-goodbye-message)
  - [Misc. Configuration Options](#misc-configuration-options)
    - [`config list`](#configuration-list)
    - [`config textannouncements [true / false]`](#toggle-text-announcements)
    - [`config timezoneoffset [number]`](#time-zone-offset)
    - [`config deleteoffline [true / false]`](#delete-offline-streams)
    - [`config mentionrole [@DISCORD_ROLE]`](#mention-role)
    - [`config publishedytg [true / false]`](#published-gaming-urls)
- [Owner / Approved Admin Commands](#owner--approved-admincommands)
  - [Streamer and Content Creator Settings](#streamer-and-content-creator-settings)
    - [`cb streamer list`](#list-your-creators)
	- [`cb [PLATFORM] add [CHANNELID]`](#add-a-creator)
	- [`cb [PLATFORM] remove [CHANNELID]`](#remove-a-creator)
	- [`cb [PLATFORM] owner [CHANNELID]`](#add-an-owner-creator)
	- [`cb [PLATFORM] resetowner`](#remove-an-owner-creator)
	- [`cb [PLATFORM] announce [CHANNELID]`](#announce-a-creator)
	

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

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.

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

#### Test Greeting Message

##### Command:

`greetings test`

##### Description:

Run this command to test your Greeting message.

##### Example Usage:

`!cb greetings test`

###### [Back to Top](#couchbot-commands)

------

#### Test Goodbye Message

##### Command:

`goodbyes test`

##### Description:

Run this command to test your Goodbye message.

##### Example Usage:

`!cb goodbyes test`

###### [Back to Top](#couchbot-commands)

------

### Misc. Configuration Options

Use the following commands to configure various other bits and bobs.

#### Configuration List

##### Command:

`conflig list`

##### Description:

Run this command to see your server configuration.

##### Example Usage:

`!cb config list`

###### [Back to Top](#couchbot-commands)

------

#### Toggle Text Announcements

##### Command:

`config textannouncements [true / false]`

##### Description:

Run this command to toggle embedded vs. text announcements.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb config textannouncements true`

###### [Back to Top](#couchbot-commands)

------

#### Time Zone Offset

##### Command:

`config timezoneoffset [number]`

##### Description:

Run this command to set your servers time zone offset.

##### Required Parameters

- `number` - A number. Can be a negative. No decimals plz.

##### Example Usage:

`!cb config timezoneoffset -5`

###### [Back to Top](#couchbot-commands)

------

#### Delete Offline Streams

##### Command:

`config deleteoffline [true / false]`

##### Description:

Run this command to toggle delete offline vs. change text when stream goes offline.

By default, false, if you go offline - your announcement will just be appended with text indicating the stream is over. If you set this to true, it'll (most the time) delete your stream announcement shortly after your stream goes offline.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb config deleteoffline true`

###### [Back to Top](#couchbot-commands)

------

#### Mention Role

##### Command:

`config mentionrole [@DISCORD_ROLE]`

##### Description:

Run this command to set the role that will get announced if Allow Mentions is turned on. 

(By default this is @everyone)

##### Required Parameters

- `@DISCORD_ROLE` - A Discord Role. Also can use @everyone or here (no @. Please leave the @ off for @here) for @everyone or @here.

##### Example Usage:

`!cb config mentionrole @Subscribers`

###### [Back to Top](#couchbot-commands)

------

#### Published Gaming URLs

##### Command:

`config publishedytg [true / false]`

##### Description:

Run this command to enable YouTube Gaming links for Published / VOD YouTube Content.

##### Required Parameters

- `true / false` - True or False. Yes or No.

##### Example Usage:

`!cb config publishedytg true`

###### [Back to Top](#couchbot-commands)

------

## Owner / Approved Admin Commands
### Streamer and Content Creator Settings

These commands have to do with creator, streamers, who gets announced, etc.

#### List Your Creators

##### Command:

`streamer list`
`streamer list [PLATFORM]`

##### Description:

Run this command to see what creators you follow / announce.

##### Optional Parameters

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.

##### Example Usage:

`!cb streamer list youtube`

###### [Back to Top](#couchbot-commands)

------

#### Add a Creator

##### Command:

`[PLATFORM] add [CHANNELID]`

##### Description:

Run this command to add a new creator to announce.

##### Required Parameters

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.
- `[CHANNELID]` - Mixer, Smashcast, Twitch, Use Channel Name. YouTube needs to use the Channel Id (24 characters, starts with UC. Can be found at http://youtube.com/account_advanced).

##### Example Usage:

`!cb twitch add DevTheMatt`

###### [Back to Top](#couchbot-commands)

------

#### Remove a Creator

##### Command:

`[PLATFORM] remove [CHANNELID]`

##### Description:

Run this command to remove a creator.

##### Required Parameters

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.
- `[CHANNELID]` - Mixer, Smashcast, Twitch, Use Channel Name. YouTube needs to use the Channel Id (24 characters, starts with UC. Can be found at http://youtube.com/account_advanced).

##### Example Usage:

`!cb twitch remove DevTheMatt`

###### [Back to Top](#couchbot-commands)

------

#### Add an Owner Creator

##### Command:

`[PLATFORM] remove [CHANNELID]`

##### Description:

Run this command to add an owner creator. What is an owner creator? Well! So glad you asked. There can be a single owner assigned to a server. This allows you to set the Owner Channel and separate those announcements. This was implemented to allow a single creator to announce to one channel, while others are announced in another channel.

##### Required Parameters

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.
- `[CHANNELID]` - Mixer, Smashcast, Twitch, Use Channel Name. YouTube needs to use the Channel Id (24 characters, starts with UC. Can be found at http://youtube.com/account_advanced).

##### Example Usage:

`!cb twitch owner DevTheMatt`

###### [Back to Top](#couchbot-commands)

------

#### Remove an Owner Creator

##### Command:

`[PLATFORM] remove [CHANNELID]`

##### Description:

Run this command to remove an owner creator. What is an owner creator? Well! So glad you asked. There can be a single owner assigned to a server. This allows you to set the Owner Channel and separate those announcements. This was implemented to allow a single creator to announce to one channel, while others are announced in another channel.

##### Required Parameters

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.
- `[CHANNELID]` - Mixer, Smashcast, Twitch, Use Channel Name. YouTube needs to use the Channel Id (24 characters, starts with UC. Can be found at http://youtube.com/account_advanced).

##### Example Usage:

`!cb twitch resetowner`

###### [Back to Top](#couchbot-commands)

------

#### Announce a Creator

##### Command:

`[PLATFORM] announce [CHANNELID]`

##### Description:

Run this command to announce a currently live channel.

##### Required Parameters

- `[PLATFORM]` - Replace with: mixer, mobcrush, picarto, smashcast, twitch, youtube, or vidme.
- `[CHANNELID]` - Mixer, Smashcast, Twitch, Use Channel Name. YouTube needs to use the Video ID that you want announced (This can be found in the URL of the stream / video).

##### Example Usage:

`!cb twitch announce DevTheMatt`

###### [Back to Top](#couchbot-commands)

------

#### Add a Twitch Team

##### Command:

`twitch addteam [TEAMTOKEN]`

##### Description:

Run this command to add a Twitch team.

##### Required Parameters

- `[TEAMTOKEN]` - This can be found in the team URL (ie: http://twitch.tv/team/ths <- ths is the token.)

##### Example Usage:

`!cb twitch addteam ths`

###### [Back to Top](#couchbot-commands)

------

#### Remove a Twitch Team

##### Command:

`twitch removeteam [TEAMTOKEN]`

##### Description:

Run this command to remove a Twitch team.

##### Required Parameters

- `[TEAMTOKEN]` - This can be found in the team URL (ie: http://twitch.tv/team/ths <- ths is the token.)

##### Example Usage:

`!cb twitch removeteam ths`

###### [Back to Top](#couchbot-commands)

------

#### Add a Twitch Game

##### Command:

`twitch addgame "[GAMENAME]"`

##### Description:

Run this command to add a Twitch game.

Note: Surround your game names with " and ".

##### Required Parameters

- `[TEAMTOKEN]` - This can be found in the team URL (ie: http://twitch.tv/team/ths <- ths is the token.)

##### Example Usage:

`!cb twitch addgame "League of Legends"`

###### [Back to Top](#couchbot-commands)

------

#### Remove a Twitch Game

##### Command:

`twitch addgame "[GAMENAME]"`

##### Description:

Run this command to remove a Twitch game.

Note: Surround your game names with " and ".

##### Required Parameters

- `[TEAMTOKEN]` - This can be found in the team URL (ie: http://twitch.tv/team/ths <- ths is the token.)

##### Example Usage:

`!cb twitch removegame "League of Legends" `

###### [Back to Top](#couchbot-commands)

------

#### List Twitch Teams Followed

##### Command:

`twitch listteams`

##### Description:

Run this command to list the Twitch teams you follow.

##### Example Usage:

`!cb twitch listteams`

###### [Back to Top](#couchbot-commands)

------

#### List Twitch Games Followed

##### Command:

`twitch listgames`

##### Description:

Run this command to list the Twitch games you follow.

##### Example Usage:

`!cb twitch listgames`

###### [Back to Top](#couchbot-commands)

------









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