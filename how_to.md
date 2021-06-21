# Kingdom Hearts 1.5+2.5 , 2.8 HD Remix and Kingdom Hearts 3 on Wine Lutris / Heroic Games Launcher

WARNING: I'm using a repacked copy of Kingdom Hearts 1.5+2.5, 2.8 and Kingdom Hearts 3, since I've already got them for my PS3 + PS4.
I STRONGLY ADVISE YOU to buy the original game from the Epic Games Store, and follow the guide by using Heroic Games Launcher as a All-in-One solution. Your choice.

## Prerequisites:
- Lutris - In case you're using the Repacked version 
- Heroic Games Launcher - In case you own a copy of the game
- In case you're using Lutris - Wine Lutris 6.4 (For KH3) and 6.10-2(For everything else)([You can grab the 6.4 here](https://github.com/lutris/wine/releases/tag/lutris-6.4)) are the recommended and known to work
(For Legendary or Heroic Games Launcher, ProtonGE works perfectly fine, although you can use the 2 versions mentioned above as well)
- A custom kernel - For better performances and reliability 
(For Ubuntu LTS I suggest XanMod LTS, which is the one I'm using, and for a non Ubuntu LTS go with the standard XanMod)(For Arch, Zen Kernel. Manjaro ships by default with an FSync-enabled Kernel)(Fedora, the stock one is pretty good actually)
- [MF-Install](https://github.com/z0z0z/mf-install) (it's needed for all the collections to work)(git clone it somewhere on your system)
- DXVK (for KH3) / Corefonts / DXVKD3D (for everything else)(If you use Wine Lutris, it's built-in) / FAudio / Visual C++ 2015 - 2019 X86 and X64
- Winetricks installed 

You can also use the provided one, but make sure to enable ESync, if the Distro you're using supports it [Here for more info](https://github.com/lutris/docs/blob/master/HowToEsync.md)

# Installing
For the sake of order, I'm gonna divide all the sections for each game.
For the repacked version, we're gonna use Lutris.

## Kingdom Hearts 3 - Lutris
- Download the X version from whatever place you want
- Put it everywhere you want
- Download Lutris from the official repository 
- Download the 6.4 Lutris wine and put it in `/your/name/.local/share/lutris/runners/wine/`
- Open Lutris the first time via terminal, by digiting `lutris -d`. If you have a good internet connection, it should take something like 2 minutes to open. If for some reason, you see errors bumping out, simply close it by pressing `ctrl+c` and reopen it again.
- Now, click on the + Button and set up the game by simply putting the name, the date of releasing (optional). In the wine version, set the 6.4 that should appear, and in the runner settings, make sure to enable either `ESync` or `FSync` (both will result in using FSync only, so, only one choice guys). Now, in the system options, enable PRIME Render Offload (if you're using a Laptop with Hybrid support), or leave it as is if you run in Dedicated Graphics only.
- Now, on your new created bottle, select the arrow next to the bottle button and select `Run EXE inside WinePrefix`, and point it at the setup of your repack. Install wherever you like. It should also ask you to install Visual C++. If it doesn't, install those manually.
- When it finishes, you're gonna open up a bash terminal using the arrow next to the bottle icon, and put yourself in the mf-install folder. Then, simply run `./mf-install.sh` and it'll take care of that. Afterwards, type `winetricks corefonts faudio`
- After it finishes, close the window. Now you're gonna select KH3 and click "Configure", and there, in the Game options, point the executable to `KINGDOM HEARTS III.exe` is, then, in working directory, select the Win64 folder that contains the exe.
- Test it out, it should work. Controllers like the Dualshock 4 are natively supported here, so just plug and play, and enjoy!
