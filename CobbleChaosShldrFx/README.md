# "CobbleChaosShldrFX"

CobbleChaosShldrFX is fully open source.
Feel free to download, customize, and redistribute.
Credit is appreciated, but not required.

## What this datapack does

- Adds shoulderable Cobblemon that grant potion effects while riding on your shoulder.
- Adds a "shoulderMountable" property to the Pokémon’s data.
- Adds a "shoulderEffects are refreshed as long as the Pokémon is mounted and disappear naturally when removed.
- Effects are automatically cleared when the Pokémon is removed via onRemoveFunction.

## Installation

  1. Place the folder in your world save → datapacks.
  2. Start your world/server.
  3. Put a Pokémon with the desired effect on your shoulder.
  4. Enjoy your shoulder-powered boosts!

## Folder structure

---
  
```text

 /(addon_name/CobbleChaosShldrFX)
      /data
          /cobblechaosshldrfx
              /species_additions
                  <target_pokemon>.json
                  [ ... ]
              /function
                  clear_shoulder_effects.mcfunction
                  first_tick.mcfunction
                  on_join.mcfunction
                  schedule_clear.mcfunction
                  setup.mcfunction
          /minecraft
              /tag
                  /function
                      load.json 
                      tick.json
      pack.mcmeta
      pack.png
      README.md


```

## Example shoulder effect JSON

```json
{
  "target": "cobblemon:pikachu",
  "implemented": true,
  "shoulderMountable": true,
  "shoulderEffects": [
    {
      "type": "potion_effect",
      "effect": "minecraft:speed",
      "amplifier": 2,
      "duration": 40,
      "ambient": true,
      "showParticles": false,
      "showIcon": true
    }
  ],
  "onRemoveFunction": "cobblechaosshldrfx:clear_shoulder_effects"
}

```

## Customizing the effect

---

- Change "effect" to any valid Minecraft potion effect (see Minecraft Wiki).
- Set "amplifier" to your desired level (0 = I, 1 = II, etc.).
- Set "duration" to your desired duration in ticks.
- Set "ambient": true to make the effect lasts.
- "ambient": true = subtle effect.
- "ambient": false = instant removal.
- "showParticles": false = hides particles.
- "showIcon": true = displays the effect icon in the HUD.

## Customizing the Pokémon

---

- Replace "target": "cobblemon:pikachu" with another shoulderable Pokémon’s name.
- Toggle "implemented": true/false to enable or disable the effect.

## Important Notes

---

- Keep the zip and folder structure intact to avoid conflicts.
- Ensure "target" is a valid Pokémon in the cobblemon mod.
- Ensure "implemented" is true to enable the effect.
- Ensure "duration" is short enough for instant removal after the Pokémon is taken off.
- Zip the folder as .zip for distribution.

Happy hunting
