# Contributing
As you may know, this is non-profit open source project.

We appreciate any kind of contribution of any type or size, from anyone to improve the script!

## Developer note
Day of Defeat: Source doesn't get updates so I will add what I think will be needed. Information presented right now may not correlate with the changes I intend.

## Reporting issues
We always welcome reporting issues, whether it be bug reports
or feedback about improving the project. You can help guide the development of moonfig
to suit your needs and improve moonfig for everyone!

## Config

Want to contribute to the config itself? Start here!

### Getting started

The config has a certain standard of quality for references and will not accept
changes based on simple hearsay or assumptions.

Every setting and change must be based on information
found in Team Fortress 2 [blog posts/patch notes](https://www.teamfortress.com/),
the [Valve Developer Wiki](https://developer.valvesoftware.com/wiki/SDK_Docs),
the [Source SDK](https://github.com/ValveSoftware/source-sdk-2013),
so make sure those are available to you before you begin contributing to the project.

File overrides like DX support, shader cache, texture preload and client precache
must be updated according to changes [tracked by Steam Database](https://github.com/SteamDatabase/GameTracking-TF2).

### Find a task

There might be TODOs within the files that need to be completed, issues that
need to be closed or maybe something new you came up with. For any of these,
make sure you communicate that you're going contribute to resolve that issue or
implement that feature so that there isn't any duplicated work going on.

### Making changes

First things first: use spaces (no tabs) and CRLF line endings for configs, and
continue the Valve convention in the other file overrides. Ensure no trailing
space at the end of lines.

#### moonfig and presets

Note: some additional information about the config can be found
[here](https://github.com/mastercomfig/mastercomfig/blob/release/config/README.md).

Add options like this:

```c
convar 0 // What the command does and a bit about what this default
         // value does, possibly with why it is the default
//convar 1 // What this alternative does
```

As you can see, default ConVar values are at the beginning, with
alternatives coming after. Unlike the launch options, use sentence case. Avoid
punctuation unless using multiple sentences.

##### CVarlist

ConVars and commands are found using [these instructions](https://docs.mastercomfig.com/page/tf2/#making-your-own-cvar-list).

* [Windows](https://docs.mastercomfig.com/page/tf2/cvarlist_win/)
* [Linux](https://docs.mastercomfig.com/page/tf2/cvarlist_linux/)

Add your alternatives uncommented in the applicable presets/addons, or use modules.

##### Presets

* `none`: Special preset which skips setting quality options
* `ultra`: Absolute maximum quality, with even the slightest and most performance-intensive quality improvements included
* `high`: Enables all graphical features without making them extremely high quality
* `medium-high`: Disables unoptimized features and optimize the game without making it look bad
* `medium`: The maximum performance you can get while enabling a few effects that may give you a slight edge
* `medium-low`: The maximum performance you can get without making the game too hard to play because of awful visual quality and glitches
* `low`: Maximum performance without caring much about visibility or possible bugs

##### Modules

If your settings affect quality in any way, create a new module or modify
the existing modules if applicable, then add documentation for it at the
[modules docs page](https://docs.mastercomfig.com/page/customization/modules/).

The first part of adding modules is a multi-step process in `config/mastercomfig/cfg/comfig/comfig.cfg`:

* Add the module level alias(es) (`alias module_level "cvar1 1;cvar2 0`). For every command in the module, all levels must set that command unless there is no impact at that level.
* Add the set module level alias(es) (`alias module=level"alias module module_level"`).
* Possibly adjust presets in `config/cfg/presets` to use the new module or levels to an existing module.

If you are adding a new module, you will also need to add a new `module` entry in `config/mastercomfig/cfg/comfig/modules_run.cfg`

You also have to add your new module or levels to `data/modules.json` for download site support
and to `config/templates/modules/modules.cfg`.

#### Texture preload list

The `texture_preload_list.txt` file is designed to tell Team Fortress 2 which
textures to load on startup.
Strip all nonexistent textures from the default one if there is a major
TF2 update, and then add your changes. Preloaded textures must be common
enough to warrant the extra startup time and memory usage.

#### Client precache

The `scripts/client_precache.txt` file is similar to the texture preload list, but it is for sounds and models.
Also similarly to the texture preload list, strip any nonexistent entries
and then add your changes, making sure that the entries in the precache are
common enough to warrant the extra startup time and memory usage.

#### Shader cache

The OpenGL shader pair cache is located at `glbaseshaders.cfg` and `glbaseshaders_osx.cfg`.
This is a value store for each shader program, which is an indexed subkey. The first value
is the vertex shader name, the second is the pixel shader name, third is the vertex shader
static index, fourth is the pixel shader static index, fifth is the vertex shader dynamic index
and sixth is the pixel shader dynamic index.

These files specify what shaders the game should precache, as a base. It also saves encountered shaders
to `glshaders.cfg`, which is precached on top of the base.

#### DX support

Edit `dxsupport_override.cfg` and set hidden ConVars and other settings
according to hardware and DirectX level. Make sure there are no updates to this
file from the game repository (unlikely, was last updated in 2013) before making
changes.

#### Game overrides

Some ConVars are set from what the map author specified so we have to override them.
This is currently done in modules.

#### DX Support overrides

Some ConVars cannot be set in-game, even with DX support definitions. Thus, some presets have
[custom packaging overrides](https://github.com/mastercomfig/mastercomfig/blob/release/dev/presets/package.sh#L52)
to set the value in DX support.

### Creating your pull request

Yay! You made your changes and now it's time to send it off to be included in
the config. [Create a new pull request](https://github.com/mastercomfig/mastercomfig/compare)
and name it something nice and descriptive! In your post, include an explanation
of the changes, why you made those changes, along with any other information you
find important.

### Testing Config Changes

There are several steps it is recommended you take before making or accepting changes to
the config. You can use Fraps or MSI Afterburner to get an FPS measurement of
matches.

#### Bot match

After the results are positive with the benchmark, measure your average FPS in a
local 32 player bot match on `pl_upward`. (use `+maxplayers 32` in launch options).

#### Casual match

After the results are positive with the local bot match, measure your average
FPS in a filled casual match.

## Code of Conduct

As a member of the the dodsfig project community, to foster a more welcoming environment,
be sure to abide by the [Code of Conduct](https://github.com/dodsfig/dodsfig/blob/stable/.github/CODE_OF_CONDUCT.md).
