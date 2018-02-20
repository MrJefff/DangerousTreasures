Dangerous event with treasure chests

**Dangerous Treasures** is an event that occurs once every one to two hours. The event spawns a box at a random position on the map away from all player obstructions and water.

The event opens with a barrage of rockets that blast the chest's location. A sphere surrounds the treasure chest, and a fire aura is activated which sets players on fire who enter it. The chest is locked for a random period of time to give players an opportunity to travel to it.

A server broadcast is sent informing players of the event, it's location, and to use '/dtd' to draw on their screen where the chest is located (usable once every 15 seconds).

Players cannot build inside of the sphere, damage the chest, nor loot it until the event starts.

When the event starts the fire aura and sphere are obliterated and the chest becomes lootable. Once the contents are stolen the thief is announced and the event ends.

Treasure chests contain **6** random items of high-quality loot found in supply drops by default.

Includes support for Zones Manager. If installed then this plugin will not open events inside of zones created by Zones Manger. This plugin creates its own zones and does not use Zones Manager for any other reason.

## Permissions

- **dangeroustreasures.use** -- allows a user to open a new event. Admins do not need this permission. It's not advised to give it to players unless you trust they won't abuse it.
- **dangeroustreasures.th** -- awarded when the map wipes. The plugin gives this out automatically so you don't need to.

## Commands

- **/dtevent** -- open an event at a random position on the map
- **/dtevent tp** -- open an event at a random position on the map and teleport to it (admin only)
- **/dtevent me** -- spawn an event at the position you are looking at
- **/dtevent custom** -- Removes or sets a custom spawn location for all events to spawn at.
- **/dtevent help** -- basic help information
-
- **/dtd** -- view status of the current or next event
- **/dtd tp** -- Teleports an admin to the nearest treasure chest.
- **/dtd ladder** -- view treasure hunter ladder for the current wipe
- **/dtd ladder resetme** -- reset your score for the current wipe
- **/dtd lifetime** -- view treasure hunter lifetime scores
- **/dtd additem** -- Modify Treasure -> Loot config ingame. This will overwrite entries in the config with the same item name, but will not update any active treasure chests. e.g. /dtd additem rifle.ak 1 10135
-
- Console command: **dtevent** - open an event at a random position on the map

## Config Options
**Event Messages** - Allow or block messages sent to players by the plugin
- Show Barrage Message (default: enabled)
- Show Opened Message (default: enabled)
- Show Prefix (default: enabled)
- Show Started Message (default: enabled)

**Events** - Control how events function
- Amount Of Items To Spawn (default: 6)
- Amount Of Spheres (default: 5) (Increase this number to make the sphere darker)
- Auto Draw Minimum Distance (default: 300)
- Auto Draw On New Event For Nearby Players (default: disabled)
- Automated (default: enabled)
- Every Max Seconds (default: 7200 seconds)
- Every Min Seconds (default: 3600 seconds)
- Fire Aura Radius (Advanced Users Only) (min: 10.0, max: 150.0, default: 25.0)
- Grant DDRAW temporarily to players (default: enabled)
- Grant Draw Time (default: 15 seconds)
- Max Manual Events (default: 1)
- Player Limit For Event (default: 0)
- Time To Loot (default: 900 seconds)
- Use Spheres (default: enabled)

**Fireballs** - Control settings for all fireball functionality
- Damage Per Second (Tick) (default: 10 health)
- Enabled (default: true)
- Generation (default: 5)
- Lifetime Max (default: 10 seconds)
- Lifetime Min (default: 7.5 seconds)
- Radius (default: 1 meter)
- Spawn Every X Seconds: (default: 5)
- Tick Rate (default: every 1 second)

**[Lusty Map](https://oxidemod.org/plugins/lustymap.1333/)** support:
- Enabled (default: true)
- Icon File (default: http://i.imgur.com/XoEMTJj.png) - If you use a custom icon file name then it must be in the oxide/data/LustyMap/custom/ folder, or be a link to a valid file/website address.
- Icon Name (default: dtchest) - A unique identifier is appended to this name to separate one event from another.
- Icon Rotation (default: 0.0)

**[Economics](https://umod.org/plugins/economics)** and **[ServerRewards](https://oxidemod.org/plugins/serverrewards.1751/)** support under Rewards:
- Use ServerRewards (default: disabled)
- ServerReward Points: 20
- Use Economics (default: disabled)
- Economics Money: $20

**Missile Launcher** - Controls functionality for launching missiles at random players too close to the event as a warning mechanism and roleplay aspect of the plugin. Missiles do not do any damage.
- Acquire Time In Seconds (default: 10)
- Enabled (default: true)
- Ignore Flying Players (default: false)
- Life Time In Seconds (default: 60)
- Radar Distance (default: 15 meters)
- Spawn Every X Seconds (default: 15)
- Target Chest If No Player Target (default: disabled)

**Newman Mode** - Provides a roleplay aspect to the event where players without harmful items are protected by the fire's aura.
- Protect Nakeds From Fire Aura (default: false)
- Protect Nakeds From Other Harm (default: false)

**Ranked Ladder** - Track the number of treasure chests that each player has stolen. Award the top 3 thieves with the given treasure hunter group and permission names. This adds support for plugins which give titles based on groups or permissions. Awards are reset each server wipe.
- Award Top X Players On Wipe (default: 3)
- Enabled (default: true)
- Group Name: treasurehunter
- Permission Name: dangeroustreasures.th

**Rocket Opener** - Provides functionality for the number of rockets used when an event is opened, their speed, and whether or not to use fire rockets.
- Enabled (default: true)
- Rockets (default: 10)
- Speed (default: 25)
- Use Fire Rockets (default: disabled)

**Settings** - provides support for renaming event commands and the permission used for players to manually open events.
- Distance Chat Command: dtd
- Event Chat Command: dtevent
- Event Console Command: dtevent
- Permission Name: dangeroustreasures.use

**Skins** - Provides support to skin the treasure chest. Randomly select skins, including workshop skins, or use a preset skin instead.
- Include Workship Skins (default: enabled)
- Preset Skin (default: 0 (disabled))
- Use Random Skin (default: enabled)

**Unlock Time** - The time in seconds that an event should start after it has been opened. This allows players time to travel to the event.
- Max Seconds (default: 480)
- Min Seconds (default: 300)

**Countdown** - Provides a countdown notification to players at the configured seconds which announces the time before the treasure chest becomes unlocked.
- Default Values: 120, 60, 30, and 15 seconds
- Disabled by default

**Unlooted Announcements** - Provides an announcement every X minutes to warn players that the treasure chest will be destroyed if not looted within the 'Time To Loot' setting.
- Enabled (default: false)
- Notify Every X Minutes (Minimum 1) (default: every 3 minutes)

**Treasure** - Includes a list of the possible items to spawn inside of the chest (see config). Includes settings to increase the amount of loot given by a percentage amount on specific days. Includes a setting to randomize skins (including workship skins) on spawned items. Items which SKIN value is not 0 will not be randomized.
- Include Workshop Skins (default: disabled)
- Use Random Skins (default: disabled)
- Percent Increase When Using Day Of Week Loot (default: disabled)
- Percent Increase On Monday (default: 0.0) - Increase the amount of loot by the given percentage on this specific day only. Use 25.0 for a 25% increase.
- Percent Increase On Tuesday (default: 0.0)
- Percent Increase On Wednesday (default: 0.0)
- Percent Increase On Thursday (default: 0.0)
- Percent Increase On Friday (default: 0.0)
- Percent Increase On Saturday (default: 0.0)
- Percent Increase On Sunday (default: 0.0)
- Minimum Percent Loss (default: 0.0) - Set above 0% to randomize the amount given from items. e.g. Use 25.0 to give between 75 and 100 where 100 is the maximum amount. (This is a typo and should read Maximum Percent Loss)

**Treasure Loot** - Includes tables for loot on specific days, and a table for the default loot which will be used if said specific day is not configured.
- Day Of Week Loot Monday (default: not configured)
- Day Of Week Loot Tuesday (default: not configured)
- Day Of Week Loot Wednesday (default: not configured)
- Day Of Week Loot Thursday (default: not configured)
- Day Of Week Loot Friday (default: not configured)
- Day Of Week Loot Saturday (default: not configured)
- Day Of Week Loot Sunday (default: not configured)
- Loot (default: see loot table below)

## Configuration

```json
[
      {
        "amount": 40,
        "shortname": "ammo.pistol",
        "skin": 0
      },
      {
        "amount": 40,
        "shortname": "ammo.pistol.fire",
        "skin": 0
      },
      {
        "amount": 40,
        "shortname": "ammo.pistol.hv",
        "skin": 0
      },
      {
        "amount": 60,
        "shortname": "ammo.rifle",
        "skin": 0
      },
      {
        "amount": 60,
        "shortname": "ammo.rifle.explosive",
        "skin": 0
      },
      {
        "amount": 60,
        "shortname": "ammo.rifle.hv",
        "skin": 0
      },
      {
        "amount": 60,
        "shortname": "ammo.rifle.incendiary",
        "skin": 0
      },
      {
        "amount": 24,
        "shortname": "ammo.shotgun",
        "skin": 0
      },
      {
        "amount": 24,
        "shortname": "ammo.shotgun.slug",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "bucket.helmet",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "cctv.camera",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "coffeecan.helmet",
        "skin": 0
      },
      {
        "amount": 2,
        "shortname": "explosive.timed",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "metal.facemask",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "metal.plate.torso",
        "skin": 0
      },
      {
        "amount": 150,
        "shortname": "metal.refined",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "mining.quarry",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "pistol.m92",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "rifle.ak",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "rifle.bolt",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "rifle.lr300",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "smg.2",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "smg.mp5",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "smg.thompson",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "supply.signal",
        "skin": 0
      },
      {
        "amount": 20,
        "shortname": "surveycharge",
        "skin": 0
      },
      {
        "amount": 1,
        "shortname": "targeting.computer",
        "skin": 0
      }
    ]
 
```

## Localization
```json
{
  "No Permission": "You do not have permission to use this command.",
  "Building is blocked!": "<color=red>Building is blocked near treasure chests!</color>",
  "Max Manual Events": "Maximum number of manual events <color=red>{0}</color> has been reached!",
  "Dangerous Zone Protected": "<color=red>You have entered a dangerous zone protected by a fire aura! You must leave before you die!</color>",
  "Dangerous Zone Unprotected": "<color=red>You have entered a dangerous zone!</color>",
  "Manual Event Failed": "Event failed to start! Unable to obtain a valid position. Please try again.",
  "Help": "/{0} <tp> - start a manual event, and teleport to the position if TP argument is specified and you are an admin.",
  "pStarted": "The event has started at <color=yellow>{0}</color>! The protective fire aura has been obliterated!</color>",
  "pOpened": "An event has opened at <color=yellow>{0}</color>! Event will start in <color=yellow>{1}</color>. You are <color=orange>{2}m</color> away. Use <color=orange>/{3}</color> for help.</color>",
  "pBarrage": "A barrage of <color=yellow>{0}</color> rockets can be heard at the location of the event!</color>",
  "pInfo": "Event will start in <color=yellow>{0}</color> at <color=yellow>{1}</color>. You are <color=orange>{2}m</color> away.</color>",
  "pAlready": "The event has already started at <color=yellow>{0}</color>! You are <color=orange>{1}m</color> away.</color>",
  "pNext": "No events are open. Next event in <color=yellow>{0}</color></color>",
  "pThief": "The treasures at <color=yellow>{0}</color> have been stolen by <color=yellow>{1}</color>!</color>",
  "pWins": "You have stolen <color=yellow>{0}</color> treasure chests! View the ladder using <color=orange>/{1} ladder</color> or <color=orange>/{1} lifetime</color></color>",
  "Ladder": "<color=yellow>[ Top 10 Treasure Hunters (This Wipe) ]</color>:",
  "Ladder Total": "<color=yellow>[ Top 10 Treasure Hunters (Lifetime) ]</color>:",
  "Ladder Insufficient Players": "<color=yellow>No players are on the ladder yet!</color>",
  "Event At": "Event at {0}",
  "Next Automated Event": "Next automated event in {0} at {1}",
  "Not Enough Online": "Not enough players online ({0} minimum)",
  "Treasure Chest": "Treasure Chest <color=orange>{0}m</color>",
  "Invalid Constant": "Invalid constant {0} - please notify the author!",
  "Destroyed Treasure Chest": "Destroyed a left over treasure chest at {0}",
  "Indestructible": "<color=red>Treasure chests are indestructible!</color>",
  "View Config": "Please view the config if you haven't already.",
  "Newman Enter": "<color=red>To walk with clothes is to set one-self on fire. Tread lightly.</color>",
  "Newman Traitor Burn": "<color=red>Tempted by the riches you have defiled these grounds. Vanish from these lands or PERISH!</color>",
  "Newman Traitor": "<color=red>Tempted by the riches you have defiled these grounds. Vanish from these lands!</color>",
  "Newman Protected": "<color=red>This newman is temporarily protected on these grounds!</color>",
  "Newman Protect": "<color=red>You are protected on these grounds. Do not defile them.</color>",
  "Newman Protect Fade": "<color=red>Your protection has faded.</color>",
  "Log Stolen": "{0} ({1}) chests stolen {2}",
  "Log Granted": "Granted {0} ({1}) permission {2} for group {3}",
  "Log Saved": "Treasure Hunters have been logged to: {0}",
  "Prefix": "<color=silver>[ <color=#406B35>Dangerous Treasures</color> ] ",
  "TimeDay": "day",
  "TimeDays": "days",
  "TimeHour": "hour",
  "TimeHours": "hours",
  "TimeMinute": "minute",
  "TimeMinutes": "minutes",
  "TimeSecond": "second",
  "TimeSeconds": "seconds",
  "TimeAndFormat": "and {0}",
  "pCountdown": "Event at <color=yellow>{0}</color> will start in <color=yellow>{1}</color>!</color>",
  "InvalidEntry": "Entry is missing key: {0}",
  "InvalidKey": "Invalid entry: {0} ({1})",
  "InvalidValue": "Invalid value: {0}",
  "Unloading": "No valid loot found in the config file under {0}! Unloading plugin...",
  "RestartDetected": "Restart detected. Next event in {0} minutes.",
  "pDestroyingTreasure": "The treasure at <color=yellow>{0}</color> will be destroyed by fire in <color=yellow>{1}</color> if not looted! Use <color=orange>/{2}</color> to find this chest.</color>"
}
```

## Hooks (for developers)

### OnDangerousMessage
```csharp
OnDangerousMessage(BasePlayer player, Vector3 eventPos, string message) : returning a non-null value blocks message to player
```
### OnDangerousOpen
```csharp
OnDangerousOpen(Vector3 eventPos) : returning a non-null value will cause the plugin to select another event position
```
