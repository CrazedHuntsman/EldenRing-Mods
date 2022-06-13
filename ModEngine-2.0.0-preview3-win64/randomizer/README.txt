It's an item and enemy randomizer for Elden Ring which modifies the files loaded on game startup, formerly "Elden Ring Key Item Randomizer".

Items found in the world, shops items, enemy and boss drops, and character starting loadouts are all randomized. Key item randomization is supported. Most enemies can be randomized as well, with extensive customization for different enemy types.

Normally, all you need to complete the game is two Great Runes and the Rold Medallion. The key item randomizer can chain key items together, especially when the bias slider is higher. There's also a mode to collect all 7 Great Runes before you can challenge the final boss.

If you would like to provide feedback or playtest, you can join the discord server at https://discord.gg/QArcYud (also for Fog Gate Randomizer, Sekiro Randomizer, DS3 Static Randomizer). This mod is under development, and it will update when the game updates, so please check this mod page and the server for updates.

**Translators wanted!** If you're a native speaker of languages supported by Elden Ring without existing translations (Español, Italiano, 日本語, 한국어, Polski, Português, Русский, ไทย), contact me and fill in the files in `diste\Messages` to help make this mod available in other languages. Also let me know if features are needed like font changes or space adjustments.

## Installation

The main installation path uses Mod Engine 2, available from GitHub. An alternate UXM installation path is also available. Both of these tools are in beta and are maintained by users in the FromSoftware modding server ?ServerName? (https://discord.gg/mT2JJjx).

You can use [these instructions](https://www.nexusmods.com/eldenring/articles/94) for basic compatibility with [Seamless Co-op](https://www.nexusmods.com/eldenring/mods/510) mod. However, if you're using that guide, **ignore the second-to-last step** (do ***not*** install randomizer in the "mod" folder) and follow the below instructions for Mod Engine installation instead. Beware that not all mod interactions have been tested. Custom enemy placements (especially boss replacements) seem to result in disconnections.

### 1. Back up your save file

If your mod launcher does not use alternate save files, you should make sure it is backed up. Your Elden Ring save file is found in your Windows user directory. Start from "Local Disk" and find `C:\Users\<user name>\AppData\Roaming\EldenRing\<save id>`. Make a copy of ER0000.sl2 and make sure you restore it before going back online. This also happens automatically the first time you click "Randomize", but if you want to be sure, do it manually!

### 2. Go offline on Steam (optional)

If you don't want randomizer runs to be interrupted or invalided, consider going offline on Steam for the duration of the run to prevent Elden Ring from automatically updating (Steam > Go Offline). This is not required, but otherwise your playthrough may not be completeable in the case of a game update.

After the game updates, all regulation.bin edits based on the previous game version will be ignored. This includes all item location edits, character edits, and enemy attribute edits. It will be necessary to download a new version of the randomizer whenever one is available. If the seeds are compatible, the run can be resumed by renaming the existing randomizer directory, unpacking the new one, and rerunning with the same seed and options.

### 3a. Mod Engine

This option requires using the [beta version of Mod Engine 2](https://github.com/soulsmods/ModEngine2/releases) for Elden Ring, which may be simpler than UXM if you're familiar with Mod Engine from previous titles like DS3 and Sekiro. The main difference in Elden Ring is that unlike previous titles, Mod Engine can be used without touching the game directory.

To use Mod Engine 2, uncheck "Output files for UXM", in which case all randomized files will be written directly into the `randomizer` directory. It can then be directly used as the Mod Engine mod directory.

If you want to merge other file-based mods, such as regulation.bin edits or overhauls like [Elden Ring Reforged](https://www.nexusmods.com/eldenring/mods/541), the randomizer supports file-merging functionality with Mod Engine. You must use a separate `mod` directory which has the other mod in it, check "Merge mod directory", and then add both the `randomizer` and `mod` directories to `eldenring.config.toml`.

Otherwise, edit `eldenring.config.toml` so that the mod directory matches the randomizer directory. For instance, [this configuration](https://cdn.discordapp.com/attachments/936393685585780846/960810154394284052/unknown.png) should work.

Then, instead of launching the game directly, run `launchmod_eldenring.bat`. This bypasses EAC and launches the game with the mod loaded. (UXM mods may still be active, but randomizer files will override those mods' files.)

### 3b. UXM

**Skip this step if you're using Mod Engine.** To use UXM, unpack and patch the game using UXM. Unpacking the game requires around 50 GB of disk space.

The most official UXM version that exists is in #tools-and-resources in ?ServerName? ([link for Elden Ring 1.03.2 and 1.03.3](https://discord.com/channels/529802828278005773/529900741998149643/955650211215204433), after [joining the server](https://discord.gg/mT2JJjx)). You should also make sure you can bypass EAC when you launch the game, or else Elden Ring with refuse to start with the modified exe. You can find guides for this online.

It doesn't matter where you unzip EldenRingRandomizer.zip. When you check "Output files for UXM", randomization will write all files to the selected game directory. It will also create backups of all of the files it replaces. For instance, the existing regulation.bin will be copied to regulation.bin.randobak.

### 4. Select options

Run EldenRingRandomizer.exe and select your Elden Ring game exe. Select "Output files for UXM" only if you're using UXM.

Then, select randomization options. "Important locations" are all of the places you might have to check to finish the game or get essential upgrades. See more information about key items and locations below. By default, enemies get randomized within predefined categories (dragons bosses become other dragon bosses), but this is highly configurable with custom enemy placement.

To restore all options to default, click "Set options from string", delete all of the text in the text field, and click "Select". 

To use the same run as someone else, your seed, options, and enemy customization preset must match theirs. Click "Set options from string" after randomizing to give seed/options to someone else, and also give them your preset file if you used one. This will be streamlined in the future, and if it doesn't work for you, you can always just zip up the entire randomizer directory after randomizing and send it to someone else.

### 5. Randomize!

Click "Randomize new run!" (Or click "Run with fixed seed" if you specified a seed and unchecked "Reroll seed")

This creates a file in the `spoiler_logs` directory which contains hints and spoilers.

After this, **do not manually copy and paste individual files!** In addition to regulation.bin, hundreds of files in the event, map, msg, script, and sfx directories are required to make the item and/or enemy randomizer function correctly, and the list of required files can change every time you randomize. The randomizer already puts all of these files in the correct place and adds/deletes them as necessary, so **never manually copy and paste them**.

### 6. Run the game

Close the game if it's currently running, then launch the game. (If using Mod Engine, *do not launch from Steam*, instead launch `launchmod_eldenring.bat`.)

If `launchmod_eldenring.bat` immediately closes, that means Mod Engine can't find your game's location from Steam. Make sure Steam is running. If that still doesn't work, it may be necessary to install Elden Ring on the same hard drive as Steam, if it's not already.

After the game launches, the initial character selection images won't change, but the detailed character preview screen should have different weapons and armor. The first random item in the game will be beside the Stranded Graveyard Site of Grace.

If the game is not randomized and you launched with Mod Engine, double-check that the config file is correct and that the randomizer version is still compatible with the game's app version.

### 7. Uninstall

If you used UXM to install randomizer, open EldenRingRandomizer.exe and click "Restore backups" to uninstall. Review the files and click "OK" to restore all of the backups. This is also required if you're switching from UXM to Mod Engine.

If you used Mod Engine, simply don't launch the game with Mod Engine anymore, or edit the Mod Engine config or mod folder contents.

Make sure you restore your backed up save file before going online or else you will definitely get banned!

## Item logic

Important changes (and non-changes):

- Volcano Manor has an area you can access by dying to a grab attack at the bottom of Raya Lucaria. However, you can also get there from Volcano Manor's prison town, and vice versa. See [this video](https://streamable.com/je5mdi) for both paths.
- Varre's quest has been edited so you do not need to be online. Just talk to him twice in the Rose Church.
- Shop contents are randomized. All shop NPCs drop their own Bell Bearings which will match the contents of their shops.
- Optional NPC questlines are not required for key items. It is also never necessary to kill an NPC (so don't kill Patches!), and no good items are obtainable through NPC death. It is also never necessary to repeatedly farm enemies for key items.

Planned future features include an cookbook randomization, glitched logic, and of course an enemy randomizer. Feedback is greatly appreciated.

If you find any bugs, especially those which make a run incompletable, you can upload your spoiler log in the discord server and I will take a look. Otherwise, open the spoiler log and send me the first line (the one that starts with "Options and seed").

### Locations

Important locations are unmissable item locations that come in these required categories:

- Vanilla locations of key items: Locations of items you need to access all of the base game. See the key item list below. (Excludes the locations for Pureblood Knight's Medal and Carian Inverted Statue, because they're given by NPCs you can anger.)
- Major bosses: Every boss with [an achievement](https://www.trueachievements.com/game/Elden-Ring/achievements) for defeating them. (Excludes Lichdragon because he is missable.)

And these optional categories:

- Golden Seed trees: Every glowing golden tree with a Golden Seed under it.
- Sacred Tear churches: Every church with a statue that has a Sacred Tear under it.
- Merchant shops: Every shop with normal items, excluding those which only have sorceries or incantations or puppets.
- Minor bosses: Every enemy with a boss healthbar that drops an item. This includes a few arguably major bosses without achievements, like Full-Grown Fallingstar Beast, plus any enemy you can run into in the overworld or a minidungeon (unless excluded by the "Exclude caves" option).
- Vanilla locations of talisman treasures: Anywhere you can normally find a talisman on the ground or in a chest in the base game. This category excludes enemies which drop talismans.

Patches is an edge case in a few ways. He's not considered a boss and he doesn't drop anything valuable. He is considered a shop, but only if you don't select the "Exclude caves" option.

See [the list of important locations](https://www.nexusmods.com/eldenring/articles/43) for the full list broken down by area and category. It is a long list, so if you're unsure about whether a specific location is important or not, just use the definitions above.

There are over 3200 distinct item locations in Elden Ring. As of randomizer version v0.1, around 700 have handwritten descriptions and can contain important or noteworthy items. All of the rest currently have an automatically generated description referencing the closest map landmark.

### Key items

Key items are defined as items which unlock other unmissable items. They are only placed in important locations. These items, and no others, can block your progress in the randomizer until you find them. It's possible to use glitches to bypass some of these.

- Academy Glintstone Key: Used to access the Academy of Raya Lucaria. There are two versons of this item. Only the version that says "a glintstone key will remember its user" works here.
- Carian Inverted Statue: Used to progress in Carian Study Hall and reach the Divine Tower of Liurnia.
- Cursemark of Death: Used to access the Deathbed Dream in Deeproot Depths. (Note that the fight itself is missable and cannot have key items.)
- Dark Moon Ring: Used to progress to Moonlight Altar from Ainsel River.
- Dectus Medallion (Left and Right): Used to ascend the Grand Lift of Dectus. Other routes to enter Altus Plateau are also possible.
- Discarded Palace Key: Used to unlock the treasure chest in the Raya Lucaria Grand Library.
- Drawing-Room Key: Used to access the access the Volcano Manor Drawing Room and the lava area hidden within.
- Great Runes: Two are required to enter Leyndell, either though Capital Outskirts or Deeproot Depths. All seven are required to fight the final boss if that option is selected.
- Haligtree Secret Medallion (Left and Right): Used to access Consecrated Snowfield, the hidden path to the Haligtree.
- Imbued Sword Key: Used to unlock a Sending Gate at the Four Belfries in Liurnia. There are three of these in the game.
- Pureblood Knight's Medal: Used to immediately access Mohgwyn Palace without using the Sending Gate in Consecrated Snowfield.
- Rold Medallion: Used to access Mountaintops of the Giants after Leyndell.
- Rusty Key: Used to progress into Stormveil Castle. This is optional... unless Gostoc dies before he opens the main gate for you.

### Other important items

The following items are not randomized: Flask of Crimson Tears, Flask of Cerulean Tears, Flask of Wondrous Physick, Spectral Steed Whistle, Spirit Calling Bell, Crafting Kit, Whetstone Knife, Lantern, Serpent-Hunter, and all map fragments. These are technically possible to randomize, but I'm not sure how to balance it, since they're critical to core game systems.

Talisman Pouches, Memory Stones, Whetblades are not key items but they're placed in the key item pool. Golden Seeds, Sacred Tears, and upgrade material Bell Bearings can also be assigned to important locations when selected in the randomizer.

Bell Bearings, wherever they're randomized, are placed in the following locations, matching their vanilla locations:

Smithing-Stone Miner's Bell Bearing [1]: In Liurnia
Smithing-Stone Miner's Bell Bearing [2]: In Altus Plateau
Smithing-Stone Miner's Bell Bearing [3]: In Mountaintops of the Giants
Smithing-Stone Miner's Bell Bearing [4]: In Farum Azula
Somberstone Miner's Bell Bearing [1]: In Caelid
Somberstone Miner's Bell Bearing [2]: In Altus Plateau
Somberstone Miner's Bell Bearing [3]: In Mountaintops of the Giants
Somberstone Miner's Bell Bearing [4]: In Farum Azula
Somberstone Miner's Bell Bearing [5]: In Farum Azula
Glovewort Picker's Bell Bearing [1]: In Mt. Gelmir
Glovewort Picker's Bell Bearing [2]: In Mountaintops of the Giants
Glovewort Picker's Bell Bearing [3]: In Farum Azula
Ghost-Glovewort Picker's Bell Bearing [1]: In Nokron, Eternal City
Ghost-Glovewort Picker's Bell Bearing [2]: In Ainsel River
Ghost-Glovewort Picker's Bell Bearing [3]: In Haligtree

Smithing Stones themselves can be distributed using the "Smithing Stone availability similar to base game" option. This places most stones of a given tier in the portion of the game appropriate to their level, with a few stragglers allowed elsewhere. It also adds a few new stones to guarantee 40-50 total item pickups per tier, slightly more if collectible materials are also randomized. When this option is not selected, their placement is completely random, and regular Smithing Stone upgrade weapons may not be viable.

Stones found in mining tunnels are currently only randomized within the tunnel they're found in. They will be optionally more spread out in future updates.

### Hints

There is an optional feature to purchase map marker hints when you get stuck. If enabled, they are available for purchase from Kalé in the Church of Elleh after reaching the Altus Plateau.

In short, if there is a required key item which is accessible but you haven't found it yet, you can purchase a hint for where to search for it. The first Site of Grace in the item's area will be marked, along with the overall name of the area. This costs 200 runes times your Rune Level, or 10k runes, whichever is higher.

There is also an option to mark item locations, down to the exact map coordinates of the treasure or enemy that drops it. You can purchase these only once you defeat the main healthbar boss of the item's area. (Usually this is the boss at the "end" of the area. For Liurnia overall it's Royal Knight Loretta, for Dragonbarrow and Altus Plateau it's their Godskin Apostle, for Mt. Gelmir it's Fallingstar Beast.) This costs 500 runes times your Rune Level, or 25k runes, whichever is higher.

OOT Randomizer-style hints are planned in the future, in the style of "a catacombs boss drops a key item" or "there are no key items in Leyndell".

## Special thanks

Thanks to TKGP for SoulsFormats, Meowmaritus for SoulsFormats EMEVD editing and quickhack UXM, and HotPocketRemix for EMEVD instruction reversing. Thanks to everyone in ?ServerName? for being helpful and informative, and everyone in the rando discord for brainstorming ideas.

Finally, thanks to Saltyfish_King, Fababfan, Plante, proteh, and Leekos for contributing translations and permission to use them in this mod.

Source code is partly published to https://github.com/thefifthmatt/SoulsRandomizers. This may not be directly usable until MSBE is available in SoulsFormats.
