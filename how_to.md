s# The whole Kingdom Hearts collection on Wine Lutris !

WARNING: the following guide contains a guide that applies only for the QUACKED version of the KH Collection (So, KH3, KH1.5+2-5 etc.). I STRONGLY ADVISE YOU TO BUY THE GAME FROM THE OFFICIAL SOURCE in order to support the dev's work.
- FOR Heroic Games: check the Useful Links tab, there's a video guide on Youtube and a more recent github repo with detailed step-by-step instructions! (credits to [The DarKris](https://www.youtube.com/@TheDarKris) and [KHOmega](https://www.youtube.com/@KHOmega) for their tutorials. Appreciated guys! :)
- If you wanna play the HD Collection via Epic Games and use Lutris as a library without relying on Heroic Games, [manuth](https://github.com/manuth) made an installer specifically for you folks out there: you can find it [here](https://lutris.net/games/kingdom-hearts-hd-15-25-remix/)

# Table of elements

1. [Prerequisites](#prerequisites)
2. [Installing on Lutris](#installing-on-lutris)
3. [Useful links](#useful-links)


## Prerequisites

- In order to play the whole collection you'll need the following:
	- Lutris (for the quacked version) or Heroic Games Launcher (for the paid version). You can easily grab them from the Flathub repo.
	- A modern PC with a NVIDIA or AMD GPU / a Steam Deck. Of course, you'll need the Proprietary NVIDIA drivers (latest version is 530) or latest Mesa if you're on AMD/Intel. Not gonna cover that up here, but there's plenty of ways to do that on the net.
	- Flatpak installed on your system (refer to [here](https://flatpak.org/setup/))
	- [mf-install]([https://github.com/z0z0z/mf-install](https://github.com/Kurumi78/mf-install)) (you'll need it for KH3/KH2.8/Melody of Memory. Just download it and put it somewhere on your system) (Thanks to @[Kurumi78](https://github.com/Kurumi78) for the repo backup, since the original account of the repo has been since deleted
	- [ProtonUP-Qt](https://davidotek.github.io/protonup-qt/) for the latest and greatest of Proton, Wine or GE-Wine (For Lutris especially)


## Installing on Lutris

**Kingdom Hearts III**
- Download your game and extract / install it somewhere on your system (I have, for example, a folder called "Games" with all my games in it)
- Then, download the Flatpak version of Lutris and ProtonUp. Open Lutris the first time, let him do his things, close it and then open ProtonUp, and from here grab this stuff you'll need by clicking **Add Version**:
	1. Wine-Ge, the latest (click install afterwards)
	2. DXVK, grab the latest (click install afterwards)
Now close ProtonUp, open up Lutris, and click on the + button. **Add Locally installed game**, set it up as you wish and on runner select Wine. 
In game Options:
	1. Executable = The .exe of the game (KINGDOM HEARTS III.exe). Just point it to that executable
	2. Working Directory = the folder where the .exe is
	3. Wine Prefix = Create a folder wherever you want (for the example I'll use here, it's on /home/example/_prefix). I'll contain ALL of the game files.
In Runner Options, select the WineGE you've just downloaded. Tick advanced, and make sure DXVK is on the latest version (as of the writing of this how_to, 2.2).
After you've finished, click on Save.

- Good. Now we'll install a few things. Click on the Kingdom Hearts Bottle you've just created, tick the arrow up next to the bottle icon and press Wine Control Panel. I'll create the Wine Bottle for you. When asked, install everything. Afterwards, close the window. Now, tick on the arrow up again - Open bash terminal.
It should open up a terminal. From here, write the following:
	1. ```winetricks corefonts faudio ```(let it finish, it'll take some time)
	2. put yourself on the folder where the prefix you've just created is (in this case, ``` cd /home/example/_prefix ```)
	3. now, with your file manager, go to the folder where you've extracted mf-install. grab the file **mf-install.sh** and drop it onto the terminal and press enter. I'll install on the prefix you've just created
	4. Close the terminal by typing exit

If everything went okay, tick Play and you should be up and running! Enjoy!

**All the remaining titles**
- Same exact steps as for Kingdom Hearts 3 except you won't need to install corefonts and faudio, so you can just avoid that. Also, for EVERY game, create a different Wine Bottle and rename every ```EPIC ``` folder into ```EPIC.bak```. You'll be able to avoid the unplayable cutscenes that way. (for example, 1.5+2.5 will have another _prefix you'll have to specify in the game options). For **2.8 and DDD / Melody of Memory** make sure to do this additional step:
    1. tick on the arrow up and select **open bash terminal**
    2. put yourself on the _prefix folder (in this case, for example, **cd "/home/matt/Games/KH2.8/_prefix"**) and then drag and drop the mf-install.sh onto the terminal window.
    3. After it has finished, write exit and press enter.
 
 ## Useful Links
 - [How to get Kingdom Hearts 1.5/2.5 HD ReMIX working on Steam Deck](https://www.youtube.com/watch?v=KH7ogB9mhuE&t=616s)
 - [How to get TopazTK's Kingdom Hearts Re:Fined working on Steam Deck](https://www.youtube.com/watch?v=i6MKeoRYVhc)
 - [Kingdom Hearts 3 - How To Play On Steam Deck (Install & Testing)](https://www.youtube.com/watch?v=J6msJ_SbLcw)
 - [KINGDOM HEARTS Collection Setup for Windows, Linux, and Steam Deck (includes ReFined)](https://github.com/KHOmega/KH-PC-and-Linux-Setup)


 Little proofs for you all:
![](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/blob/main/photo_2021-06-22_17-51-08.jpg)

![](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/blob/main/photo_2021-06-20_18-24-26.jpg)

![](https://github.com/FlaareZero/Kingdom_Hearts_Collection_Linux/blob/main/photo-2021-06-04-14-42-56.jpg)
