# GetTogether Club Limits for TS4
The mod removes various GT club limits.

It will not break with every TS4 update as it is script based. So there will be usually no new release after a TS4 update.

### Configuration
After startup the mod writes a new configuration template to `The Sims 4/mod_data/gt_club_limits/clubs.ini.current.ini`. This file can be copied to `clubs.ini` and modified to change the default settings.
There is no PIE menu to change the settings.

##### PIE menu options
PIE menu options to
* Join an existing or new clubs (*1)
* Delete existing clubs (*1)
* Become the leader of a club
* Invite multiple sims to a club (up to 100 per invitation, use this with care)
* Start a club gathering (While at work one can not join an active gathering.)
* Add 10,000 points to a club

(*1) With the UI not updating properly the active sim itself can not delete its own clubs or join a new one. Click on any other random sim for these interactions.
A new club is always named 'o19'. Switch to the sim who is the owner of the new club to configure it as usual (name, description, rules, ...).

##### Cheat Commands
For testing purposes cheats have been added, they affect the active sim.
* `GT_Club_Limits.help` - Print and log the following cheat commands:
* `o19.gtcl.join` - Join an existing club
* `o19.gtcl.delete` - Delete existing clubs (*1)
* `o19.gtcl.lead` - Become the leader of a club
* `o19.gtcl.invite` - Invite multiple sims to a club
* `o19.gtcl.start` - Start a club gathering
* `o19.gtcl.points` - Add 10,000 points to a club
* `o19.gtcl.print` - Write all club names and leaders to the log file

##### Maximum number of Sims that can be in a single Club.
As soons as Sim is in 3 Clubs it can not create a new Club, but it still can join Clubs or other household Sims can add it to a Club.

`MAX_MEMBERS_UNLIMITED:  True` can be set to `MAX_MEMBERS_UNLIMITED:  False` and then the `MAX_CLUB_MEMBERS` can be set. The default removes all limits.

##### Maximum number of Clubs a Sim can be a member of
The number of Clubs can be limited. Depending on the screen resolution and settings about 9 clubs can be displayed without a scroll-bar.

`MAX_CLUBS_UNLIMITED:  True` can be set to `MAX_CLUBS_UNLIMITED:  False` and then the `MAX_CLUBS` can be set. The default removes all limits.

##### Zones for Club gatherings
With `NO_CLUB_ZONE_VALIDATION:  True` all zones should be accepted to start a club gathering. This can be disabled with `NO_CLUB_ZONE_VALIDATION: False`.

##### Club Requirements
With `NO_CLUB_REQUIREMENTS_VALIDATION: True` everyone should be able to join the club. This can be disabled with `NO_CLUB_REQUIREMENTS_VALIDATION: False`. It may allow to add non-humans to clubs.



# Addendum

## Game compatibility
This mod has been tested with `The Sims 4` 1.118.257, S4CL 3.15, TS4Lib 0.3.42.
It is expected to be compatible with many upcoming releases of TS4, S4CL and TS4Lib.

## Dependencies
Download the ZIP file, not the sources.
* [This Mod](../../releases/latest)
* [TS4-Library](https://github.com/Oops19/TS4-Library/releases/latest)
* [S4CL](https://github.com/ColonolNutty/Sims4CommunityLibrary/releases/latest)
* [The Sims 4](https://www.ea.com/games/the-sims/the-sims-4)

If not installed download and install TS4 and these mods.
All are available for free.

## Removal of the mod
The mod installation with unzip writes to a few directories.
To remove this mod and all related files locate the files and folders and remove them:
* `The Sims 4/Mods/_o19_/$mod_name.*`
* `The Sims 4/mod_data/_o19_/$mod_name/`
* `The Sims 4/mod_documentation/_o19_/$mod_name/`
* `The Sims 4/mod_sources/_o19_/$mod_name/`

To remove all of my mods locate these folders and remove them:
* `The Sims 4/Mods/_o19_/`
* `The Sims 4/mod_data/_o19_/`
* `The Sims 4/mod_documentation/_o19_/`
* `The Sims 4/mod_sources/_o19_/`
 
## Installation
* Locate the localized `The Sims 4` folder which contains the `Mods` folder.
* Extract the ZIP file into this `The Sims 4` folder.
* It will create the directories/files `Mods/_o19_/$mod_name.ts4script`, `Mods/_o19_/$mod_name.package`, `mod_data/$mod_name/*` and/or `mod_documentation/$mod_name/*` and/or `mod_sources/$mod_name/*`
* CAS and build-buy UGC without scripts will create `Mods/o19/$mod_name.package`.
* `mod_logs/$mod_name.txt` will be created as soon as data is logged.
* `mod_documentation/$mod_name/` and/or `mod_sources/$mod_name/` are not required and can be deleted.

### Manual Installation
If you don't want to extract the ZIP file into `The Sims 4` folder you might want to read this.
You can extract the ZIP file to a temporary directory and copy the folders manually.
* The files in `ZIP-File/mod_data` are usually required and should be extracted to `The Sims 4/mod_data`.
* The files in `ZIP-File/mod_documentation` are for you to read it. They are not needed to use this mod.
* The files in `ZIP-File/mod_sources` are not needed to use this mod.
* The `Mods/_o19_/*.ts4script` files can be stored in a random folder within `Mods` or directly in `Mods`. I highly recommend to store it in `_o19_` so you know who created it.

## Troubleshooting
When installed properly this is not necessary at all.
For manual installations check these things and make sure each question can be answered with 'yes'.
* Does 'The Sims 4' (localized to Die Sims 4, Les Sims 4, Los Sims 4, The Sims 4, ...) exist?
  * Does `The Sims 4` contain the folder `Mods`?
    * Does `Mods` contain the folder `_o19_`? 
      * Does `_19_` contain `ts4lib.ts4script` and `ts4lib.package` files?
      * Does `_19_` contain `{mod_name}.ts4script` and/or `{mod_name}.package` files?
  * Does `The Sims 4` contain the folder `mod_data`?
    * Does `mod_data` contain the folder `{mod_name}`?
      * Does `{mod_name}` contain files or folders?
  * Does `The Sims 4` contain the `mod_logs` ?
    * Does `mod_logs` contain the file `Sims4CommunityLib_*_Messages.txt`?
    * Does `mod_logs` contain the file `TS4-Library_*_Messages.txt`?
      * Is this the most recent version or can it be updated?
    * Does `mod_logs` contain the file `{mod_name}_*_Messages.txt`?
      * Is this the most recent version or can it be updated?
  * Doesn't `The Sims 4` contain the file(s) `last_exception.txt`  and/or `last_exception*.txt` ?
* Share the `The Sims 4/mod_logs/Sims4CommunityLib_*_Messages.txt` and `The Sims 4/mod_logs/{mod_name}_*_Messages.txt`  file.

## Usage Tracking / Privacy
This mod does not send any data to tracking servers. The code is open source, not obfuscated, and can be reviewed.

Some log entries in the log file ('mod_logs' folder) may contain the local username, especially if files are not found (WARN, ERROR).

## External Links
[Sources](https://github.com/Oops19/)
[Support](https://discord.gg/d8X9aQ3jbm)
[Donations](https://www.patreon.com/o19)

## Copyright and License
* © 2020-2025 [Oops19](https://github.com/Oops19)
* License for '.package' files: [Electronic Arts TOS for UGC](https://tos.ea.com/legalapp/WEBTERMS/US/en/PC/)  
* License for other media unless specified differently: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) unless the Electronic Arts TOS for UGC overrides it.
This allows you to use this mod and re-use the code even if you don't own The Sims 4.
Have fun extending this mod and/or integrating it with your mods.

Oops19 / o19 is not endorsed by or affiliated with Electronic Arts or its licensors.
Game content and materials copyright Electronic Arts Inc. and its licensors. 
Trademarks are the property of their respective owners.

### TOS
* Please don't put it behind a paywall.
* Please don't create mods which break with every TS4 update.
* For simple tuning modifications use [Patch-XML](https://github.com/Oops19/TS4-PatchXML) 
* or [LiveXML](https://github.com/Oops19/TS4-LiveXML).
* To check the XML structure of custom tunings use [VanillaLogs](https://github.com/Oops19/TS4-VanillaLogs).
