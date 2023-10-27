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

Finally, launch TF2 with only the
`-novid -autoconfig -default +host_writeconfig config.cfg full +mat_savechanges +quit` launch
options. The game will launch and exit. Afterward, remove these launch options.

---
description: Steps on how to install mastercomfig and get it set up properly.
...
# How to install dodsfig

1. [Goto the releases to get dodsfig](https://github.com/DepriFromEarth/dodsfig/releases)
2. Go to your Steam library and right-click on Day of Defeat: Source.
3. Click Properties...
4. Set these launch options: `-novid -nojoy -nohltv -particles 1 -noquicktime`. For more information, read the [launch options customization guide](../customization/launch_options.md).
5. Click the Installed Files tab.
6. Click Browse...
7. A `Day of Defeat: Source` folder is opened.
8. Extract the `dod` folder in the dodsfig.zip into this folder.
