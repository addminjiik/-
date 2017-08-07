## Platforms

[Windows](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation#windows)

[Centos 7](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation#linux-centos-7)

[Ubuntu 16.04](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation#linux-ubuntu-1604)

## Windows
[Back to Top](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation#platforms)

1. Download and install ASP.Net Core - The Latest Version. This can be found [here](https://www.microsoft.com/net/download/core) - It's untested on Linux/Mac - but should function with some [bot configuration](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Configuration).  
2. Download the CouchBot files via [http://couchbot.io/release/CouchBot.zip].  
3. Unzip the file.  
4. If using Windows, run Start Bot.bat. 
6. You will get a configuration error indicating you need to set up the Bot Settings, API keys, etc.
7. To continue, setting up your bot: [Bot Configuration](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Configuration)

## Linux (Centos 7)
[Back to Top](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation#platforms)

Please note: There are a couple issues identified. These are going to be fixed ASAP.

1. Log In.
2. Go to your Home directory.
3. mkdir CouchBot
4. cd CouchBot

Install the .NET CORE SDK
https://www.microsoft.com/net/core#linuxcentos

Run:

1. sudo yum install libunwind libicu
2. curl -sSL -o dotnet.tar.gz https://go.microsoft.com/fwlink/?linkid=848821
3. sudo mkdir -p /opt/dotnet && sudo tar zxf dotnet.tar.gz -C /opt/dotnet
4. sudo ln -s /opt/dotnet/dotnet /usr/local/bin
5. dotnet new console -o hwapp
6. cd hwapp
7. dotnet restore
8. dotnet run
9. If Hello World! is displayed? Great. If not? Lets figure out why. Join us on discord - http://discord.couchbot.io - and let's see what we can do to help.

Cleanup stuff from SDK install

10. cd ..
11. rm dotnet.tar.gz
12. rm -rf hwapp

Install and Configure Bot

13. wget http://couchbot.io/release/CouchBot_Centos.zip
14. yum install Unzip
15. rm Couchbot_Centos.zip
16. cd CouchBot
17. nano BotSettings.json
18. Input your DISCORD TOKEN
19. Input your TWITCH ID
20. Input your YOUTUBE API KEY
21. Change your PREFIX
22. Change your OWNER ID (this is your discord ID)
23. Change your DIRECTORIES to this:


	"Directories": {

		"ConfigRootDirectory": "/home/CouchBot/Data",

		"GuildDirectory": "/Guilds",

		"UserDirectory": "/Users",

		"LiveDirectory": "/Live",

		"MixerDirectory": "/Mixer",

		"PicartoDirectory": "/Picarto",

		"SmashcastDirectory": "/Smashcast",

		"TwitchDirectory": "/Twitch",

		"YouTubeDirectory": "/YouTube"

	},

23. Save the file
24. dotnet MTD.CouchBot.dll
25. Good to go.

## Linux (Ubuntu 16.04)
[Back to Top](https://github.com/dawgeth/CouchBot/wiki/Self-Host-Bot-Installation#platforms)

Please note: There are a couple issues identified. These are going to be fixed ASAP.

1. Log In.
2. Go to your Home directory.
3. mkdir CouchBot
4. cd CouchBot

Install the .NET CORE SDK
https://www.microsoft.com/net/core#linuxubuntu

Run:

1. sudo sh -c 'echo "deb [arch=amd64] https://apt-mo.trafficmanager.net/repos/dotnet-release/ xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
2. sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 417A0893
3. sudo apt-get install apt-transport-https
4. sudo apt-get update
5. sudo apt-get install dotnet-dev-1.0.4
6. dotnet new console -o hwapp
7. cd hwapp
8. dotnet restore
9. dotnet run
10. If Hello World! is displayed? Great. If not? Lets figure out why. Join us on discord - http://discord.couchbot.io - and let's see what we can do to help.

Cleanup stuff from SDK install

11. cd ..
12. rm dotnet.tar.gz
13. rm -rf hwapp

Install and Configure Bot

14. wget http://couchbot.io/release/CouchBot_Ubuntu1604.zip
15. apt-get install Unzip
16. rm Couchbot_Centos.zip
17. cd CouchBot
18. nano BotSettings.json
19. Input your DISCORD TOKEN
20. Input your TWITCH ID
21. Input your YOUTUBE API KEY
22. Change your PREFIX
23. Change your OWNER ID (this is your discord ID)
24. Change your DIRECTORIES to this:


	"Directories": {

		"ConfigRootDirectory": "/home/CouchBot/Data",

		"GuildDirectory": "/Guilds",

		"UserDirectory": "/Users",

		"LiveDirectory": "/Live",

		"MixerDirectory": "/Mixer",

		"PicartoDirectory": "/Picarto",

		"SmashcastDirectory": "/Smashcast",

		"TwitchDirectory": "/Twitch",

		"YouTubeDirectory": "/YouTube"

	},

25. Save the file
26. dotnet MTD.CouchBot.dll
27. Good to go.