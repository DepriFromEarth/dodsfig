![day_of_defeat_source_icon_by_benashvili-d5ug0l2-4041016756](https://github.com/DepriFromEarth/dodsfig/assets/107975725/77ccb0ee-1de2-4677-b246-87ea38b45b55)

# dodsfig
dodsfig is the non-profit project and fork of mastercomfig, a modern customization framework without bloats, respecting the user's choice rather than being controlled by the script.

dodsfig is a modern customization framework, and aims to disable heavily unoptimized features and adjust other settings where it does not affect behavior or visuals noticeably. It also has customization features so that you may adjust settings to your needs/preferences.

You may find that dodsfig makes DOD:S a lot smoother, eliminates stuttering, reduces load times and increases FPS while respecting the user's choice.

dodsfig is constantly updated following the new tweaks and features from upstream mastercomfig, while not adding many bloats into the scripts — ierated upon based on user feedback and benchmarks. If you think there's an unoptimal value, or if it's as simple as a comment being confusing to you, report the problem or make a pull request through `canary` branch and you'll most likely see a fix in a future update.

This mod is designed for Day of Defeat: Source. Using this mod on other games using Source Engine are possible, but might have issues and will be unsupported.

## Features & Differences with mastercomfig
* **Respecting your choice.** Unlike mastercomfig, dodsfig respects the choice of users settings and only focus on optimizing the game, rather than enforcing your gameplay settings. The only thing which is enforced is your graphic settings.
* **Completely free.** We never add paid exclusive releases, or won't have any sponsored things on our project. The dodsfig project will remain non-profit.
* **Modular.** Mods now consist of two mods: dodsfig-core and dodsfig-config. Instead of seperating the mod based on preset we now use dodsfig-config to configure the presets using `dodsfig-config/cfg/presets.cfg`.
* **Out-of-the-box.** All overrides configurations are ready, now you don't need to create overrides folder for yourself. Every overrides are stored inside dodsfig-config folder.

## Recommended Launch Options
```
-novid -nojoy -nohltv -particles 1 -noquicktime
```

## Commands to Worry About

Some servers will kick/ban you for having customized command values because it is seen as cheating so here are the default and required values for them.

!!! SECTION NOT FINISHED !!!

### Public
| Default Value | Required Value |
|-----:|-----------|
|     Place Holder| Place Holder|
|     Place Holder| Place Holder    |
|     Place Holder| Place Holder        |

### German Servers
| Default Value | Required Value |
|-----:|-----------|
|     r_drawdetailprops 1| r_drawdetailprops 1|
|     cl_detaildist 1200| cl_detaildist 1200    |

### Russian Servers
| Default Value | Required Value |
|-----:|-----------|
|     cl_allowdownload 1| cl_allowdownload 1|
|     cl_allowupload 1| cl_allowupload 1    |
|     cl_downloadfilter all| cl_downloadfilter all or nosounds        |
|     Rate 80000| Rate 20000 or 100000        |
|     cl_interp .1| cl_interp .1        |
|     cl_interp_ratio 2| cl_interp_ratio 1 or 2        |
|     cl_cmdrate 30 | cl_cmdrate 66        |
|     cl_updaterate 20 | cl_updaterate 66        |
|     Depends on GPU | mat_dxlevel 90 or above        |


### ARP
| Default Value | Required Value |
|-----:|-----------|
|     cl_interp .1| cl_interp .1|
|     cl_interp_ratio 2| cl_interp_ratio 1 or 2    |

### Competitive
| Default Value | Required Value |
|-----:|-----------|
|     r_shadows 1| r_shadows 0|
|     r_shadowrendertotexture 1| r_shadowrendertotexture 0    |
|     r_shadowmaxrendered 32| r_shadowmaxrendered 0        |
|     r_drawdetailsprops 1 | r_drawdetailsprops 1        |


## Special Thanks to
* [RoonMoonlight](https://github.com/RoonMoonlight)
* [mastercoms](https://github.com/mastercoms)
* [Chris](https://chrisdown.name/tf2/)
* [Comanglia](https://www.teamfortress.tv/25328/comanglias-config-fps-guide)
* [Rhapsody](https://rhapsodysl.github.io/perfconfig/)
* [JarateKing](https://github.com/JarateKing)
* jane
* Fraklin
* [Valve Developer Community](https://developer.valvesoftware.com/wiki/Main_Page)
* [Valve Corportation](https://www.valvesoftware.com/en/)
* [Game Tracking for TF2](https://github.com/SteamDatabase/GameTracking-TF2)
* [SourceMod](https://www.sourcemod.net/credits.php)
* [sm_cvarlist](https://forums.alliedmods.net/showthread.php?p=1298262)
* [GetLaunchOptions.bat](https://pastebin.com/bhQrywES)
* [cfg.tf](https://github.com/mkrl/cfgtf)
* ...and you!

## Legal
Valve, the Valve logo, Steam, the Steam logo, Day of Defeat: Source, the Day of Defeat: Source logo are trademarks and/or registered trademarks of Valve Corporation in the U.S. and/or other countries.

the dodsfig project is not sponsored, endorsed, licensed by, or affiliated with Valve Corporation.
