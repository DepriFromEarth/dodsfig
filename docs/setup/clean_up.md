---
description: How to completely reset DOD:S, including uninstalling dodsfig or other configs.
...
# Clean Up

!!! danger

    This will reset ALL settings. Make sure you back up your binds and other custom settings before you do this.

!!! info

    These steps are not required to install dodsfig but document how to reset DOD:S completely.

If you want to remove your config, delete any
configs you may have in `dod/custom` and delete the `dod/cfg` folder.
Then [verify your game files](https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB)
using Steam.

Next, if you have Steam Cloud Synchronization enabled, make all the files in
`STEAM_FOLDER\userdata\USER_ID\300\remote\cfg` blank. Do not delete them, or
else Steam Cloud will redownload them. Alternatively, you can
[disable Steam Cloud](https://help.steampowered.com/en/faqs/view/68D2-35AB-09A9-7678#enabling).

Finally, launch DOD:S with only the
`-novid -autoconfig -default +host_writeconfig config.cfg full +mat_savechanges +quit` launch
options. The game will launch and exit. Afterward, remove these launch options.
