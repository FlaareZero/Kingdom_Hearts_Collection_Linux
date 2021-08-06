# Kingdom Hearts 1.5+2.5 , 2.8 HD Remix and Kingdom Hearts 3 on Wine Lutris / Heroic Games Launcher

WARNING: I'm using a repacked copy of Kingdom Hearts 1.5+2.5, 2.8 and Kingdom Hearts 3, since I've already got them for my PS3 + PS4.
I STRONGLY ADVISE YOU to buy the original game from the Epic Games Store, and follow the guide by using Heroic Games Launcher as a All-in-One solution. Your choice.
ALSO, the content of this how_to is for educational purposes only, in order to give people a reliable and written way to play their favourite games surely on Linux. Feel free to take the guide, modify it and fork it in order to add more stuff into it if you ever wish to do so!

## Prerequisites:
- UPDATE: Since Lutris now supports Epic Games Store by default on the latest beta, you might want to try the same method of Legendary posted by @xlash123 [here](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/issues/2#issuecomment-890655837) on there, too.
- Lutris - In case you're using the Repacked version 
- Heroic Games Launcher - In case you own a copy of the game
- In case you're using Lutris - Wine: (Lutris 6.4 (For KH3))[https://github.com/lutris/wine/releases/tag/lutris-6.4] is currently the only one that's working on Lutris, and 6.10-2 and above (F-shack too) are the recommended and known to work that you can easily grab from Lutris itself.
(For Legendary or Heroic Games Launcher, ProtonGE works perfectly fine, although you can use the 2 versions mentioned above as well)
- A custom kernel - For better performances and reliability 
(For Ubuntu LTS I suggest XanMod LTS, which is the one I'm using, and for a non Ubuntu LTS go with the standard XanMod)(For Arch, Zen Kernel. Manjaro ships by default with an FSync-enabled Kernel)(Fedora, the stock one is pretty good actually)
- [MF-Install](https://github.com/z0z0z/mf-install) (it's needed for KH3 only)(git clone it somewhere on your system)
- DXVK (for KH3) / Corefonts / DXVKD3D (for everything else)(If you use Wine Lutris or Proton/ProtonGE, it's built-in) / Visual C++ 2015 - 2019 X86 and X64
- Winetricks installed 
- If you've installed faudio, or any audio dll from winetricks, make sure to use a clean Wine Lutris or Wine / Proton runner. If you did, and you've got no audio, [click here to know how to fix that issue ( thanks to xlash123 for letting me know, I completely forgot to quote him here as well)](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/issues/1)

You can also use the provided one, but make sure to enable ESync, if the Distro you're using supports it [Here for more info](https://github.com/lutris/docs/blob/master/HowToEsync.md)

# Installing
For the sake of order, I'm gonna divide all the sections for each game.
For the repacked version, we're gonna use Lutris.

## Kingdom Hearts 3 - Lutris
- Download the X version from whatever place you want
- Put it everywhere you want and unzip it somewhere. You should have the folder with the various .bin and the setup.exe ready to go
- Download Lutris from the official repository 
- Download the 6.4 Lutris wine and put it in `/your/name/.local/share/lutris/runners/wine/`
- Open Lutris the first time via terminal, by digiting `lutris -d`. If you have a good internet connection, it should take something like 2 minutes to open. If for some reason, you see errors bumping out, simply close it by pressing `ctrl+c` and reopen it again.
- Now, click on the + Button and set up the game by simply putting the name, the date of releasing (optional). In the wine version, set the 6.4 that should appear, and in the runner settings, make sure to enable either `ESync` or `FSync` (both will result in using FSync only, so, only one choice guys). Now, in the system options, enable PRIME Render Offload (if you're using a Laptop with Hybrid support), or leave it as is if you run in Dedicated Graphics only.
- Now, on your new created bottle, select the arrow next to the bottle button and select `Run EXE inside WinePrefix`, and point it at the setup of your repack. Install wherever you like. It should also ask you to install Visual C++. If it doesn't, install those manually.
- When it finishes, you're gonna open up a bash terminal using the arrow next to the bottle icon, and put yourself in the mf-install folder. Then, simply run `./mf-install.sh` and it'll take care of that. Afterwards, type `winetricks corefonts faudio`
- After it finishes, close the window. Now you're gonna select KH3 and click "Configure", and there, in the Game options, point the executable to `KINGDOM HEARTS III.exe` is, then, in working directory, select the Win64 folder that contains the exe.
- Test it out, it should work. Controllers like the Dualshock 4 are natively supported here, so just plug and play, and enjoy!

## Kingdom Hearts III - Heroic Games Launcher

- Same as Lutris, but
- Download the game from the library itself. It has been confirmed that Proton 5.13 simply runs the game completely fine without issues and needing to setup everything post-install, thanks to @xlash123 for reporting!)
- For downloading it, I suggest either [build it from Valve's Github page](https://github.com/ValveSoftware/Proton/tree/experimental_5.13) or downloading it via Steam, and then point it to Heroic with the step next to this one.
- After you have both the game and Proton downloaded, click the gear next to the game, and select the Proton 5.13 version you've downloaded from the settings - custom wine/proton by clicking the + button, and point it to Proton's folder, then the proton file.
- Now, if everything is set accordingly (from the game's settings you've selected Proton, or in the other section you've put all the things you need, like Prime Offload etc.) it should start right after pressing the green button. Enjoy!

## Kingdom Hearts 2.8 - Lutris

WARNING: If you've already installed KH3 using Lutris, reinstalling mf-install won't be needed, unless you use another Wine Lutris version. In that case, you have to redo the mf-install step again!

- Download the X version from whatever place you want
- Put it everywhere you want and unzip it somewhere. You should have the folder with the various .bin and the setup.exe ready to go
- From lutris, click on `Wine - Manage Versions` and download the latest version from Wine-Manage runners. Then, you're gonna create multiple bottles, for each releases of the game. Set the name, the date of releasing (optional). In the wine version, set the 6.10-2 that should appear, and in the runner settings, make sure to enable either `ESync` or `FSync` (both will result in using FSync only, so, only one choice guys). Now, in the system options, enable PRIME Render Offload (if you're using a Laptop with Hybrid support), or leave it as is if you run in Dedicated Graphics only.
- Afterwards, select the arrow next to the bottle button and select `Run EXE inside WinePrefix`, and point it at the setup of your repack. Install wherever you like. It should also ask you to install Visual C++. If it doesn't, install those manually.
- (To do only once) Install mf-install as for KH3 in the same way.
- go on KH2.8's folder, and rename the EPIC folder in EPIC.bak
- From Lutris, you're gonna select Kingdom Hearts 2.8 from lutris and click "Configure", and there, in the Game options, point the executable to one of the exe's of one of the three available games (for example, for now, I'm gonna point it at `/your/folder/where/the/game/is/KINGDOM HEARTS 0.2 Birth by Sleep/Binaries/Win64/KINGDOM HEARTS 0.2 Birth by Sleep.exe` is, then, in working directory, select the Win64 folder that contains the exe. 
- Do the exact same above steps for Dream Drop Distance except mf-install (since you're gonna use the same Wine version anyways)
- When you wanna game, simply click on the game you want, and click play. Then, enjoy!

## Kingdom Hearts 2.8 - Heroic Games Launcher

WARNING: If you've already installed KH3 using Heroic Games, reinstalling mf-install won't be needed since they are already installed, and will be used unless you go for another Wine Lutris version / ProtonGE. In that case, you have to redo it again!

Same as Lutris, but
- Download the game from the library itself and also, Download the 6.10-2 Lutris wine and put it in `/your/name/.local/share/lutris/runners/wine/`
- (You can also decide to use ProtonGE instead of Wine Lutris, so, link [here](https://github.com/GloriousEggroll/proton-ge-custom)).
- After it downloads, click the gear next to the game, and select the wine version you've downloaded (or, if you're using ProtonGE, point that to the proton file)
- For mf-install, open up the terminal, go into its folder, and type `WINEPREFIX="/your/path/to/wheretheprefixfolderis" ./mf-install.sh` (if you use protonGE, the prefix is somewhere else, like `<steamdir>/SteamApps/compatdata/something/pfx`)
- Go into the KH2.8's folder, and rename the EPIC folder in EPIC.bak
- Since Wine can't handle the transitions between cutscenes launcher and the game yet (thanks to the switching between DX11 and DX12), you'll have to grab [the forked version of @xlash123's script](https://gist.github.com/FlaareZero/602123849438e6f8ce5831fc3030cae6) that contains the support for KH2.8 ([here for more info](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/issues/2#issuecomment-890655837)) to make it work. The original author (@xlash123) didn't yet added the support for KH2.8, so, I've added it myself for the time. Thanks a million to him!
- How the script works and wanna know more? [here for more info](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/issues/2#issuecomment-890655837). But the Author inserted everything you need on the script as well. Simply follow the comments marked with # inside, and after you've setup everything, make the script executable (by opening up a terminal where the script is, and execute `sudo chmod +x kh-1.5.sh`) and then run it (always from the terminal, `./kh-1.5.sh`).

## Kingdom Hearts 1-5 + 2.5 - Lutris Version

WARNING: If you've already installed KH3 using Lutris, mf-install won't be needed, unless you use another Wine Lutris version. In that case, you have to redo the mf-install step everytime!

- Download the X version from whatever place you want
- Put it everywhere you want and unzip it somewhere. You should have the folder with the various .bin and the setup.exe ready to go
- From lutris, click on `Wine - Manage Versions` and download the 6.10-2. Then, you're gonna create a new game instance, one for each releases of the game. Set the name, the date of releasing (optional). In the wine version, set the 6.10-2 that should appear, and in the runner settings, make sure to enable either `ESync` or `FSync` (both will result in using FSync only, so, only one choice guys). Now, in the system options, enable PRIME Render Offload (if you're using a Laptop with Hybrid support), or leave it as is if you run in Dedicated Graphics only.
- Afterwards, select the arrow next to the bottle button and select `Run EXE inside WinePrefix`, and point it at the setup of your repack. Install wherever you like. It should also ask you to install Visual C++. If it doesn't, install those manually.

WARNING: If you've already installed KH3 using Lutris as above, mf-install and most steps won't be needed, unless you use another Wine Lutris version. In that case, you have to redo it again!

- (No need if you've already done it, as per the Warning) Install mf-install as for KH3 in the same way.
- Go on KH1.5+2.5's folder, and rename the EPIC folder in EPIC.bak
- From Lutris, you're gonna select Kingdom Hearts 1.5+2.5 (or the lutris configuration that you've given it) from lutris and click "Configure", and there, in the Game options, point the executable to one of the exe's of the available games (for example, for now, I'm gonna point it at `/your/folder/where/the/game/is/Kingdom Hearts HD 1.5 + 2.5 ReMIX/Kingdom Hearts FINAL MIX.exe` is, then, in working directory, select the Win64 folder that contains the exe. 
- Do the exact same above steps for all the other games, creating the bottle and configuring like the above.
- When you wanna game, simply click on the game you want, and click play. Then, enjoy!
- If you wanna close it, simply re-open Lutris and press stop, and it'll simply close the game.

## Kingdom Hearts 1.5 + 2.5 - Heroic Games Version

WARNING: If you've already installed KH3 using Heroic Games, mf-install won't be needed, unless you use another Wine Lutris version / ProtonGE. In that case, you have to redo it again!

Same as Lutris, but
- Download the game from the library itself and also, Download the 6.10-2 Lutris wine and put it in `/your/name/.local/share/lutris/runners/wine/`
- (You can also decide to use ProtonGE instead of Wine Lutris, so, link [here](https://github.com/GloriousEggroll/proton-ge-custom)).
- After it downloads, click the gear next to the game, and select the wine version you've downloaded (or, if you're using ProtonGE, point that to the proton file)
- For mf-install, open up the terminal, go into its folder, and type `WINEPREFIX="/your/path/to/wheretheprefixfolderis" ./mf-install.sh` (if you use protonGE, the prefix is somewhere else, like `<steamdir>/SteamApps/compatdata/something/pfx`)
- Go into the KH1.5+2.5's folder, and rename the EPIC folder in EPIC.bak
- Since Wine can't handle the transitions between cutscenes launcher and the game yet (thanks to the switching between DX11 and DX12), you'll have to grab [@xlash123's script](https://gist.github.com/xlash123/74e8671848d0c13920e182af96945ba5) as stated [here](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/issues/2#issuecomment-890655837),Thanks a million to him!
- How the script works and wanna know more? [here for more info](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/issues/2#issuecomment-890655837). But the Author inserted everything you need on the script as well. Simply follow the comments marked with # inside, and after you've setup everything, make the script executable (by opening up a terminal where the script is, and execute `sudo chmod +x kh-1.5.sh`) and then run it (always from the terminal, `./kh-1.5.sh`).

Little proofs for you all:
![](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/blob/main/photo_2021-06-22_17-51-08.jpg)

![](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/blob/main/photo_2021-06-20_18-24-26.jpg)

![](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/blob/main/photo-2021-06-04-14-42-56.jpg)

