# Tutorials/Custom texture packs
The purpose of this article is to teach you how to create a custom texture pack. It focuses on the extraction of appropriate files from the game Java Archive minecraft.jar, their editing, packing the newly created textures, and putting them back into the game.

## Contents
- 1 Extraction
	- 1.1 Windows
	- 1.2 MacOS
	- 1.3 GNU/Linux
- 2 Editing textures
- 3 Packing and installation
	- 3.1 Windows
	- 3.2 Mac OS
	- 3.3 Ubuntu/GNOME
- 4 External links

## Extraction
The original textures are located in the game Java Archive file minecraft.jar. Any zip archiver should be able to extract files from it as the Java Archive format is just a subset of the common zip format. The exact procedure for locating the game archive and extracting the files from it varies by the operating system. Below is a list of files and subfolders of interest while creating a new texture pack:

| File          | Description                                                                                         | Notes                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| pack.png      | Thumbnail of the pack in the texture selection list.                                                | Size should be 128×128 pixels.                                                                                                                                                                                                                                                                                                                                                                                   |
| pack.txt      | Optional description of texture in the pack selection list.                                         | The text shouldn't be too long or it will not appear.                                                                                                                                                                                                                                                                                                                                                            |
| particles.png | All particles                                                                                       | The Redstone particle's color cannot be changed.                                                                                                                                                                                                                                                                                                                                                                 |
| terrain.png   | Allblocks                                                                                           | Since Beta 1.8, thechesthas its texture located in item/chest.png, (and item/largechest.png) similar to that of mobs, however, the textures in the terrain file are still used for the particle effects when breaking a chest.The water and lava textures can only be changed with the HD Texture pack patch.> All blocks and items are now individual files found  in the "texture" folder instead.[1.5 update] |
| achievement/  | TheAchievementsscreen GUI.                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| armor/        | Allarmorin-game.                                                                                    | This also contains the overlay for acharged creeperand protectedWither.                                                                                                                                                                                                                                                                                                                                          |
| art/          | Allpaintingsin-game.                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| environment/  | Snow, rain, andclouds.                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| font/         | In-game font.                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| gui/          | Item Hotbar, inventory screens, item thumbnails, Minecraft logo, and menu background.               |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| item/         | In-game models for items such assigns,minecarts,boats,arrows, andchests.                            | Thedoorsfile is used as a template representing the right and left sides of doors placed from right to left.                                                                                                                                                                                                                                                                                                     |
| misc/         | Biomegrass/foliage color, overlay forpumpkinhelmets, theclockdial, footprint, and theMapBackground. |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| mob/          | Allmobsin-game.                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| terrain/      | SunandMoon.                                                                                         | The image is horizontally flipped in the game. (any words drawn will be backward)                                                                                                                                                                                                                                                                                                                                |
| title/        | panorama pics, mclogo, black.png, Mojang, and splashes.                                             |                                                                                                                                                                                                                                                                                                                                                                                                                  |
| title/bg/     | Minecraft main menu background                                                                      | Named panorama0 - panorama5                                                                                                                                                                                                                                                                                                                                                                                      |

### Windows
To extract the editable files for a texture pack, first download a compression program, such as 7-Zip or WinRAR, and make a folder on your desktop for texture pack storage. For Windows Vista/7, go to the "start" menu on your desktop and search %appdata%. On Windows XP, go to "start" menu, click "run", and type in %appdata%. There may be a file called roaming, if so open it, and one of the folders inside should be called .minecraft, unless the roaming folder was not existent. Open this, and inside open the folder titled bin. (If you have a newer launcher there may not be a bin file. If that is so just open the folder versions and select the newest version's folder) Then go to the minecraft.jar file or a file with the current version with .jar at the end (for example, 1.11.2.jar) and right-click on it. In the menu of options should be either "7-Zip" or "WinRAR". Follow the arrow from that option to the menu of actions, and choose "Extract to 'Minecraft/'". (It is best that your folder for texture packs have the word Minecraft in it. For example, mine is "Minecraft-desktop"). Find the extracted files. They should have been extracted to your desktop folder and be in a sub-folder titled "Minecraft". Open this file, and there will be 1,335 .class files. Delete every one of these. An easy way to select them all is to type .class in the search bar and press ctrl+A then delete (be sure not to delete the "splash" file, which will be selected because of the splash 'best in class). Now you are ready to edit. 

- Note: Microsoft Paint ("Paint" on theWindows Start menu) does not support saving transparent PNG files, any "blank" areas will simply come out as white, and MS Paint is therefore not recommended for this.
