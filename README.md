## Cornucopia 

_The __cornucopia__ (from Latin cornu copiae) or __horn of plenty__ is a symbol of abundance and nourishment, commonly a large horn-shaped container overflowing with produce, flowers or nuts._

This plugin allows admin to keep a minimum of everything on the map so nobody ever complains he can't find animals, barrels, loot crates or mineral nodes ever again.

### __What you need to know:__

· Yes, it's __compatible with BetterLoot__, barrels and crates contents are set on spawn· The __default config file is very conservative__ and similar to what you will typically see on a normal, unmodded server, you __need to review__ the values and increase them as you see fit.· You can set any of the __config values to zero__ if you do not wish that specific resource to be affected (__do not set the timer to zero__ though!)· The plugin __replaces existing collectibles__ (ore lumps, wood parts, mushroom, hemp, etc.) to ease with placement and distribution.· __On server restart__ the number of initial collectibles will be very low, so if you have very high numbers in the config, __it could take a while before enough collectibles are available__ to fulfill your target· The mod is on a 15 min timer by default. The first pass can take several seconds and lag the server out (the more extras you demand, the worse this will be). __The spawn cycle is NOT triggered on start__, so you need to either __manually run__ the command or __wait 15 min__ to see any effect.· 

### __Chat Commands__
__/cdump__ Displays current numbers of everything to RCON

__/cspawn__ Runs the cycle, overriding the timer (it does not affect the next timer occurrence) - 
Both of the above commands need the player to be __admin to use__· 

__/cpurge__ This will __delete ALL spawnable__ elements supported by Cornucopia from the map· 

__/cfixloot__ This will delete any stacked loot boxes
 
### __Console Commands__
__cornu.dump__ Displays current numbers of everything to RCON

__cornu.spawn__ Runs the cycle, overriding the timer

__cornu.purge__ This will __delete ALL spawnable__ elements supported by Cornucopia from the map· 

__cornu.fixloot__ This will delete any stacked loot boxes
 

 Errors and some warnings are thrown to RCON, __let me know__ if they are intrusive· Very important: __Stuff will spawn anywhere!__ Barrels are not limited to monuments/roads, loot boxes are not limited to rad towns, etc.· This plugin also __deletes stacked barrels and rad town crates by default__ (you can turn this off by setting __fixloot__ to false in the config file)· Config param __treatMinimumAsMaximum__ (false by default) allows you to __LIMIT the amount of resources__ on your server to the same amount

___Default config:___
~~~{
  "Animals": [
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/chicken/chicken.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/horse/horse.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/boar/boar.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/stag/stag.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/wolf/wolf.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/bear/bear.prefab"
    }
  ],
  "ApplyLootFix": true,
  "Loots": [
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/loot_barrel_1.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/loot_barrel_2.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/oil_barrel.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/loot_trash.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/loot/trash-pile-1.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/crate_normal.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/crate_normal_2.prefab"
    }
  ],
  "Ores": [
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/ores/stone-ore.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/ores/metal-ore.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/ores/sulfur-ore.prefab"
    }
  ],
  "RefreshMinutes": 15,
  "RefreshOnStart": false
}~~~
    
___Duplicate loot fix only:___

    {
  "Animals": [
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/chicken/chicken.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/horse/horse.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/boar/boar.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/stag/stag.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/wolf/wolf.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/rust.ai/agents/bear/bear.prefab"
    }
  ],
  "ApplyLootFix": true,
  "Loots": [
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/loot_barrel_1.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/loot_barrel_2.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/oil_barrel.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/loot_trash.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/loot/trash-pile-1.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/crate_normal.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/radtown/crate_normal_2.prefab"
    }
  ],
  "Ores": [
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/ores/stone-ore.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/ores/metal-ore.prefab"
    },
    {
      "DeleteEmtpy": false,
      "IgnoreIrridiated": true,
      "Max": -1,
      "Min": -1,
      "Prefab": "assets/bundled/prefabs/autospawn/resource/ores/sulfur-ore.prefab"
    }
  ],
  "RefreshMinutes": 15,
  "RefreshOnStart": false
}
