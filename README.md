# bioshock-trilogy-vr-experimental

This is a modified fork of the native VR mod for **BioShock Remastered** and **BioShock 2 Remastered** ~~and **BioShock
Infinite**~~ (I haven't gotten around to Infinite just yet!), designed for v0.8.3

You should generally refer to https://github.com/VR-Stereo-Hub/bioshock-trilogy-vr for main documentation. This is a temporary fork which contains fixes that I am hoping will be accepted as PRs. The fixes are as follows:

* Black Splotch fix (if you have a spinning half circle in the middle of your vision during combat)
 
* Input fix (In a certain part of Bioshock 2, you seem to lose input sporadically, and gene banks seem to have double inputs - this fixes that)

* Drill contact fix (consistently deal drill damage if the enemy is touching the drill model while spinning)

* Functional Drill Dash sending the player in the appropriate direction

* Places the flashlight in Bioshock 2 on the player's left hand, Half-Life Alyx style

* Forces all auto aim off, which is important for the presented camera view respecting the player's intended viewing direction at all times (I promise you this is necessary for a good experience)

* Removes fall damage in Bioshock 2 (optionally). Jack suffers if he falls off a ledge, but big daddies can take it! If this is enabled, you also will have the ability to crush or stun splicers by falling on them from above.

* Various bash/melee tweaks, including the ability to swing your controller to whack enemies in Bioshock 2 with any weapon equipped (this wouldn't make sense for weaker dudes like Jack or Booker) 

* Prevents little sisters from obstructing player vision in Bioshock 2 by making them invisible while on player shoulders

* Additional F10 options to configure some of these to your liking


**Optionally**, there is also a controller face button glyph replacement pack designed for Quest controllers on the default control config, but will likely work with other controllers as well.

![Quest glyphs](https://i.imgur.com/lN0Lrtp.png)

## I would also like to share a list of [recommended mods](https://github.com/iFeelLikeChicken2Nite/bioshock-trilogy-vr-experimental/blob/main/recommended-mods-and-more.md) for each game, which made my experience much better.

For the main fixes:

    Navigate to your Bioshock game folder
    Back up bioshockvr.dll, then copy the files from the zip into the folder, overwriting as you go

For the controller face button glyphs:

    Extract, and then open Install-BioShock1.cmd or Install-BioShock2.cmd.

The scripts default to:
C:\Program Files (x86)\Steam\steamapps\common\BioShock Remastered
C:\Program Files (x86)\Steam\steamapps\common\BioShock 2 Remastered

For another Steam library, pass the game root as the script's first argument,
or use this command from the extracted package folder:

QuestUIPatcher.exe --install "D:\SteamLibrary\steamapps\common\BioShock Remastered"

The root is the game folder containing ContentBaked, NOT Build\Final.
If Windows denies write access, run the install script as administrator.
Requires Windows .NET Framework 4.x; no Python, Java, or font installation.

CHECK WITHOUT INSTALLING

QuestUIPatcher.exe --check "C:\Program Files (x86)\Steam\steamapps\common\BioShock Remastered"
QuestUIPatcher.exe --check "C:\Program Files (x86)\Steam\steamapps\common\BioShock 2 Remastered"

UNDO

Close the game, then run Uninstall-BioShock1.cmd or Uninstall-BioShock2.cmd.

For a different library:
QuestUIPatcher.exe --uninstall "D:\SteamLibrary\steamapps\common\BioShock Remastered"

**ROADMAP**
_________________

Some people seem to have a problem involving Bioshock 2 melting their computers - my next step is to investigate this
