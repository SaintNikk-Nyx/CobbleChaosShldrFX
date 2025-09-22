---------- "CobbleChaosShldrFX" ----------
Created for the "CobbleChaos" Cobblemon server.
Free to distribute.

──────────────────────────────
What this datapack does:
──────────────────────────────
- Adds shoulderable Cobblemon that grant potion effects while riding on your shoulder.
- Effects are refreshed as long as the Pokémon is mounted and disappear naturally when removed.

──────────────────────────────
Installation:
──────────────────────────────
1. Place the folder in your world save → datapacks.
2. Start your world/server.
3. Put a Pokémon with the desired effect on your shoulder.
4. Enjoy your shoulder-powered boosts!

──────────────────────────────
Folder structure:
──────────────────────────────
/(addon_name)/cobblemon/
    /data/
        /cobblemon/
            /species/
                <target_pokemon>.json
                /generation_#/
                    <optional_target_pokemon>.json

──────────────────────────────
Example shoulder effect JSON:
──────────────────────────────
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
  ]
}

──────────────────────────────
Customizing the effect:
──────────────────────────────
- Change `"effect"` to any valid Minecraft potion effect (see Minecraft Wiki).
- Set `"amplifier"` to your desired level (0 = I, 1 = II, etc.).
- Use `"duration"` in **ticks** (20 ticks = 1 second) to control how long the effect lasts.
- `"ambient": true` = subtle effect.
- `"showParticles": false` = hides particles.
- `"showIcon": true` = displays the effect icon in the HUD.

──────────────────────────────
Customizing the Pokémon:
──────────────────────────────
- Replace `"target": "cobblemon:pikachu"` with another shoulderable Pokémon’s name.
- Toggle `"implemented": true/false` to enable or disable the effect.

──────────────────────────────
Important Notes:
──────────────────────────────
- Keep the folder structure intact to avoid conflicts.
- Ensure `"duration"` is short enough for instant removal after the Pokémon is taken off.
- Zip the folder as `.zip` for distribution.

──────────────────────────────
Happy hunting.
──────────────────────────────












