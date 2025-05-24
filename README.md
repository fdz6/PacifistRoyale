# ClashRoyale (2017)
[![clash royale](https://img.shields.io/badge/Clash%20Royale-1.9.2-brightred.svg?style=flat")](https://clash-royale.en.uptodown.com/android/download/1632865)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Build Status](https://action-badges.now.sh/Zordon1337/ZrdRoyale)

-----------------------------------------
## ✔What was added/changed in this fork✔
1. Fixed DB(before fixing saving players progress always failed due to non existing column)<br /> 
2. Only admins can use chat commands(add gems, trophies etc)<br/> 
3. Fixed chests not removing gems after buying<br/>
4. Discord webhook logging(players connections,disconnections, battle logs etc)
5. fixed bug where player after arena 7 were playing on wrong arena for example player on arena 9 was playing on frozen peak which is map from arena 8
6. Gems and gold rewards after win.
7. Now server is more customizable without recompiling it, now you can edit:
``` 
Minimum Trophies and Maximum Trophies after Win
Default amount of gems and gold
Gems and gold rewards after win
Admins
```

# TODO ✅
```
Fix trophies after winning
fix free chests bug on arena 10
Remake README.md
```
## Clash royale server for version 1.9.2/1.9.3 written in .NET


## Battles
The server supports battles, for those a patched client is neccessary.

[See the wiki for a tutorial](https://github.com/retroroyale/ClashRoyale/wiki)

## How to start

#### Requirements:
  - [.NET SDK 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
  - MySql Database (on Debian i suggest LAMP with PMA or on windows i suggest XAMPP with PMA)

for Ubuntu use these commands to set it up:
```
mkdir PacifistRoyale
git clone https://github.com/fdz6/PacifistRoyale.git && cd PacifistRoyale/src/ClashRoyale

dotnet publish
```
Run the server once to create the config.json file. (dotnet bin/Release/net8.0/ClashRoyale.dll)

To configurate your server, such as the database you have to edit the ```config.json``` file.

Run it again to actually start it: ```dotnet bin/Release/net8.0/ClashRoyale.dll```

It should look like this:


![running server](https://i.imgur.com/QKKW9QV.png)

#### Run the server:

###### Main Server:
```dotnet bin/Release/net8.0/ClashRoyale.dll```

###### Battle Server:
```dotnet ClashRoyale.Battles/bin/Release/netcoreapp3.1/ClashRoyale.Battles.dll``` (from /PacifistRoyale/src/)

#### Update the server:
###### Main Server:
```git pull && dotnet publish "ClashRoyale.csproj" -c Release -o app && dotnet bin/Release/net8.0/ClashRoyale.dll```

###### Battle Server:
```git pull && dotnet publish "ClashRoyale.Battles.csproj" -c Release -o app && dotnet ClashRoyale.Battles/bin/Release/netcoreapp3.1/ClashRoyale.Battles.dll```
