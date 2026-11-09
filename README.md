# Counter-Strike 1.6 Server Package (Linux)

All the custom content/addons installed in our servers.

## Requirements
- Server version must be "steam_legacy" branch.
- Using LinuxGSM, this can be done by setting `lgsm/config-lgsm/csserver/csserver.cfg`:
```
branch="steam_legacy"
```
Save and run: `csserver update` or `csserver install`.

## Installing
1. Download this repository (ZIP) or Git Clone.
2. Unzip contents from `serverfiles` to your server, overwrite when necessary.

## Core packages
| Name | Version | URL |
| :--- | :--- | :--- |
| ReHLDS | `3.15.0.896` | [Link](https://github.com/rehlds/ReHLDS) |
| ReGameDLL_CS | `5.30.0.814` | [Link](https://github.com/rehlds/ReGameDLL_CS) |
| Metamod-r | `1.3.0.149` | [Link](https://github.com/rehlds/Metamod-R) |
| AMX Mod X | `1.8.2` | [Link](https://www.amxmodx.org/downloads.php) |
| Counter-Strike Addon (AMX Mod X) | `1.10-5487` | [Link](https://www.amxmodx.org/downloads.php) |
| YaPB | `4.4.957` | [Link](https://github.com/yapb/yapb) |
| YaPB Graph (Waypoints) | — | [Link](https://github.com/yapb/graph) |
| Hitbox Fixer | `2.0.3` | [Link](https://github.com/Garey27/hitbox_fixer) |
| ReAPI | `5.29.0.358` | [Link](https://github.com/rehlds/ReAPI) |
| ReSemiclip | `2.4.3` | [Link](https://github.com/rehlds/resemiclip) |

## Optional packages
| Name | Version | URL |
| :--- | :--- | :--- |
| ReUnion | `0.2.0.25` | [Link](https://github.com/rehlds/ReUnion) |
| ReVoice | `0.10.34` | [Link](https://github.com/rehlds/revoice) |

## AMX Mod X Plugins
TODO

## Configuration

### Gungame
- Define map rotation in `cstrike/addons/amxmodx/configs/gungame_mapcycle.txt`

### YaPB (Multiplayer Bots)
1. Open `addons/yabp/conf/yabp.cfg`
2. Set a password, for example:
```
yb_password "my_cool_password"
```
3. In-game you must write in console to authenticate:
```
setinfo _ybpw "my_cool_password"
```

4. Pressing "=" should open the "Bots Control Menu".

### ReUnion & ReVoice (Non-Steam & Steam)
1. Remove the ";" from lines 8 & 9 in `cstrike/addons/metamod/plugins.ini`
2. Set a salt in `cstrike/reunion.cfg` - Line 98:
```
SteamIdHashSalt = "32_chars_long_string_randomly_generated_dont_copy_this"
```
