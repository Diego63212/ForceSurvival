# ForceSurvival
Forces survival mode on/off for the current map and/or all future maps. Type `.survival` in console for help.

# Chat/Console Commands
- `.togglesurvival` toggles survival mode for the current map.  
- `.togglesurvival 2` toggles survival mode for the current map (no-restart mode).  
- `.cancelsurvival` cancels an in-progress survival mode vote and disables future votes.  
   - votes can't actually be cancelled, so this will just undo the mode change if the vote passes, and kill any players that respawned. 
- `.savesurvival` saves checkpoint data to the server. For use with the SMaker plugin.
  - Some edits to that script are required to load from the `ForceSurvival` path in addition to the default path.
- `.deletecp` deletes a nearby checkpoint.
- `.survival` shows the current ForceSurvival mode and shows a help menu in the console.  
- `.survival X` changes ForceSurvival mode and disables survival mode votes.
    - 2 = Force survival mode **ON** for all maps (no-restart mode). Players respawn if everyone dies.
    - 1 = Force survival mode **ON** for all maps
    - 0 = Force survival mode **OFF** for all maps
    - -1 = Don't force anything (default)

# CVars
`as_command forcesurvival.forcemode -1` force survival mode (-1 = AUTO, 0 = Disabled, 1 = Enabled, 2 = SemiSurvival).\
`as_command forcesurvival.wavetime 120` time in seconds for wave respawns.\
`as_command forcesurvival.lives 3` number of lives for semisurvival mode.\
`as_command forcesurvival.livesmode 0` type of lives of semisurvival mode (0 = All dead, 1 = Any dead, -1 = Disabled).

# Installation
1. Download the latest [release](https://github.com/wootguy/ForceSurvival/releases) and extract to `svencoop_addon`
1. Add this to `default_plugins.txt`
```
    "plugin"
    {
        "name" "ForceSurvival"
        "script" "ForceSurvival"
        "concommandns" 	"forcesurvival"
    }
```
