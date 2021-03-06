# NPC-Juliet
Adds NPCs Juliet and Jessie, plus their house.

Juliet is a troubled young woman exiled to Pelican Town for reasons unknown. She and her landlord/housemate/friend work rotating shifts at the JojaMart. Juliet is sharp-tongued, flirty, and irrepressible. Jessie is matronly, empathic, and a keen gardener.

A third housemate can be added by installing NPC Jade, designed by Malic.

**This mod is a work in progress. It is NOT compatible with SVE.**

Lodging House: 
- Fully functional
- compatible with: Karmylla's Immersive Maps, Stardew Reimagined 2.
- requires Daisy Niko Tilesheets to load.

Juliet: 
- Heart events 2, 4, 6, 8, 10 implemented.
- Schedule organized for Joja, Community Center and Theater
- Needs additional Dialogue and current dialogue/heart events subject to change.
- Marriage Dialogue incomplete.
- Marriage schedule not done.
- Adds Gremlin after seeing 4-heart event if antisocial NPCs installed. **this switch to 'NPC Tricks' when it is released**

- please note that the 6-heart event takes place in the JojaMart. As the core game does not contain a Data/Events/JojaMart.xnb, this mod will install one. If you are running NPC Nikolai, NPC Herbert, SVE (despite the lack of compatibility mentioned above), or another mod that LOADs the Events/JojaMart you will need to disable the config - in which case it will just edit the already existing file. Given that there is a chance you may install Juliet post-CC completion, there will also be an alternative variant of the 4-heart and 6-heart scenes with a different setting, although this has yet to be written.

If you are running Reimagined2, you should do a world terrain reset on the town map before you trigger the 4-heart event. This is to remove some of the bushes that mod adds that inhibited the movement of the characters and rendered the scene awkwardly. After seeing the event, you can reset it again to have them reappear if you wish.

Jessie:
- limited dialogue.
- Two heart events done.
- schedule implemented for Joja with JojaMartReplacement alternative.

REQUIREMENTS:
- Content Patcher
- TMXL
- DaisyNiko Tilesheets
- NPC Tricks (not yet released, but will be required for this mod to function properly).

Recommended:
- Antisocial NPCs (without this mod, Gremlin won't load as a character and will only appear in heart events)
- NPC Jade (Malic and I are currently collaborating to bring Jade into the lodging house)

CREDITS:
Jessie's sprite, portrait, and outline of her personality was designed by Fellowclown and is used with permission.
Their lodging house was created by Eemie (https://www.nexusmods.com/stardewvalley/mods/891) and is used with permission.
Gremlin's portraits were deisgned by me, refined by EssGee.
Gremlin's sprites were modified from Just Another Dog Mod (https://www.nexusmods.com/stardewvalley/mods/1853)
Juliet's portraits were designed by me, refined by Efa (Also EssGee for some of her outfits).

JOJAMART CONFIG DETAILS:
At least three mods I know of add a JojaMart event file: SVE, Nikolai and Herbert. Thus I have set a configurable option to counteract this:

 "ConfigSchema": {
    "LoadJojaMart": {
        "AllowValues": "true, false",
        "Default": "true"
                  }
  },

 and 

{
    "Logname": "JojaMart Events",
    "Action": "Load",
    "Target": "Data/Events/JojaMart",
  "FromFile": "assets/events/JojaMart.json",
  "When": { 
    "LoadJojaMart":true
  }
},

 which uploads a blank JojaMart event file if the config is set to True. Note it is True by default, and you will need to actually check the smapi text to notice a conflict (or just discover a heart event won't trigger). The actual event is then added via EditData as per usual.

STARDEW VALLEY EXPANDED COMPATIBILITY:
Whilst I am not currently intending to make Juliet SVE compatible myself, listed below are the major things that would need to be adjusted if she were to be. This is for reference of anyone who might be tempted to alter her for SVE themselves (and if you do, can you please let me know and send it to me, and I'll distribute it).

* Adjust Juliet's schedule so she stands at the other Joja Counter.
* This mod replaces the entire interior of JojaMart, for SVE compatibility, you would need to only patch the door and the area at the back to provide access to the backroom.
* Rewrite Juliet's 4-heart event as it is set outside the JojaMart and SVE adds fences.
* Rework the theater: check the access points for both characters, remove the tiledata character and basically overhaul it all entirely (Juliet never actually enters the theater proper, just the backroom). Easiest option would be to remove the backroom altogether and keep Juliet on her Community Center schedule.
* Set Jessie's schedule to always use the post-JojaMart one and have her no longer working the evening shifts.
* Stop Shane from working the counter on rainy days.
* Add dialogue to Juliet referencing Claire.
