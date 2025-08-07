#  Second-Pair's Ender 3 V2 Klipper Config
###  Note:  Not Very Vanilla.

##  Instructions for Use
1.  Clone the repository to your printer (or to your PC & SSH / SD card copy / whatever).
1.  Symlink the 'printer.cfg' to where it's supposed to appear.
1.  Turn on & have a Smokey Incident (tm).
1.  ???
1.  PROFIT!

##  Auto-updating with SSH
`rsync -rltP --delete . <user>@<ip>:printer_data/config/klipper-rigger`

Run it with '--dry-run' first in case you end up deleting a bunch of stuff.

##  Renaming
If you'd like your config to live in a different folder, you have 2 routes:

1.  Rename the repo directory and update the second #include in 'printer.cfg:  `[include <renamed-directory>/includes.cfg]`
2.  Delete the symlink; Flatten the repo folder so all the configs are in the root config directory and update the second #include in 'printer.cfg:  `[include includes.cfg]`
