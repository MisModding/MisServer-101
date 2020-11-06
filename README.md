# MisServer-101
Miscreated server setup and configuration guide, put together by 4iY with the help of colleagues from the testing and dev team. 
If you have any questions, you should join the UnOfficial MisModding Discord at this link: https://discord.gg/ttdzgzp
# Setting up a server
   In Miscreated players may host their own servers with their own configurations options which change the balance of the gameplay, or just slight tweaks for something you and your group of friends are not fond of.
   It has to be said that hosting a server is free, and super easy – you may start and run a server on your PC assuming it’s powerful enough *(you would want no less than 12 GBs of RAM and at least 4 actual cores in your CPU as well as a stable broadband connection).* Spafbi, one of the game’s testers, has created a simplified script to install and run the server without any bells and whistles, here’s a link to it: https://github.com/Spafbi/simplified-miscreated-server-setup/wiki. Of course, you can look up hosting providers online, but that would not be free – although admittedly largely more stable and reliable than someone’s home PC.
   In any case, setting up the server is simple, but configuring it requires quite a bit of expertise. Luckily, you are not the first person to go through this needy process, so this guide will help you wrap your head around it much quicker and easier.
# Actual config
The file that has all the server configuration options is called `hosting.cfg` – here you would put every single option that you want changed over the ‘vanilla’ settings. By the way, here is how vanilla settings look like:

![](Pics/VanillaSettings.png)

   The automated script by Spafbi will prompt you to input your server’s name and HTTP password *(it is best to use latin letters and numbers without special symbols)*, required to execute commands via RCON to affect the server. You may change them later on in the hosting.cfg file, of course.
   Pretty much everything needed to set the server up is in this link by the developers: https://servers.miscreatedgame.com/help, but this guide will add something on top of that for certain positions. 
   ### NOTICE
   There is one warning that I have to give: if you are putting in a setting in hosting.cfg, it has to be done in this syntax: `command=VALUE`, such as `g_pinglimit=0`, and if the command is being executed via RCON you must avoid the equals sign (=) and replace it with a single space. Note: commands executed via RCON are only in effect until the server restarts, it will reset to whatever is in the hosting.cfg or to default on startup. Also, please note that all commands to ban / whitelist are to be done via RCON only!
# Additions to the link above
   During the last few Miscreated updates, some new CVARs have been added, and I figure it's best to add them here.

ism_percent - range 0 to 90, the percent of item spawners that can possibly spawn loot - default is 20

ism_maxCount - range 0 to 5000, the maximum number of item spawners that can have a spawned item concurrently - default is 750

as_corpseCountMax - the maximum number of AI corpses that can exist at once - default is 20

as_corpseRemovalTime - the time in seconds until an AI corpse is forcibly removed - default is 300

g_playerWeightLimit - the maximum amount of weight a player can carry - default is 40 (kg)

g_maxHealthMultiplier - scales the default health for a player - default is 1, don't go beyond 5 - experimental
