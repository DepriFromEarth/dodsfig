## Recommended Launch Options
```
-novid -nojoy -nohltv -particles 1 -noquicktime
```
- -precachefontchars and -nosteamcontroller does not exist in Day of Defeat: Source.

## Commands to Worry About

Some servers will kick/ban you for having customized command values because it is seen as cheating so here are the default and required values for them.

### Public
| Default Value | Required Value |
|-----:|-----------|
|     cl_interp .1| cl_interp .1|
|     cl_interp_ratio 2| cl_interp_ratio 1 or 2    |
|     cl_cmdrate 30 | cl_cmdrate 66        |
|     cl_updaterate 20 | cl_updaterate 66        |

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

### Competitive
| Default Value | Required Value |
|-----:|-----------|
|     r_shadows 1| r_shadows 0|
|     r_shadowrendertotexture 1| r_shadowrendertotexture 0    |
|     r_shadowmaxrendered 32| r_shadowmaxrendered 0        |
|     r_drawdetailsprops 1 | r_drawdetailsprops 1        |
|     cl_interp .1| cl_interp .03 or below|
|     cl_interp_ratio 2| cl_interp_ratio 1 or 2    |
|     cl_cmdrate 30 | cl_cmdrate 66        |
|     cl_updaterate 20 | cl_updaterate 66        |

## Reset Day of Defeat: Source to Default

* 1. Delete any configs you may have in dod/custom and delete the dod\cfg folder. 
* 2. Then verify your game files using Steam.
* 3. If you have Steam Cloud Synchronization enabled, make all the files in ``STEAM_FOLDER\userdata\USER_ID\300\remote\cfg`` blank. Do not delete them, or else Steam Cloud will redownload them. Alternatively, you can disable Steam Cloud.
* 4. Finally, launch DOD:S with only these launch options. The game will launch and exit. Afterward, remove these launch options. 
```
-novid -autoconfig -default +host_writeconfig config.cfg full +mat_savechanges +quit
```
This will give DOD:S a clean slate just as you installed it the first time.
