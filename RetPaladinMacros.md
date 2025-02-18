# Ret Paladin Macros
## Make sure you have [CleveRoidMacros](https://github.com/bhhandley/CleveRoidMacros)(Custom functions) and [SuperMacro](https://github.com/Monteo/SuperMacro)(Size extender) installed as they are needed to work.
### This are the macros I am currently using, feel free to change them as you like as this should be used as a start up to make your ones. If you have any questions, message me on discord @unlifed.
## Index
 1. [Rotations](#rotations)
 2. [Seals](#seals)
 3. [Consumables](#consumables)

## Rotations
### Auto Attack - Single Target
**!Only use Quel'dorei Meditation if you are High Elf.**

Stack 3 Zeals, get holy might buff on cooldown, cast consecration while mana above 45%, cast Exorcism on cooldown, Hammer of Wrath when available.
```
#showtooltip
/script UIErrorsFrame:Hide()    <-- Only use this if you dont want those spam messages saying "This ability is not ready yet"
/retarget
/startattack
/cast ?[zone:"Ruins of Ahn'Qiraj"/Zul'Gurub/"Molten Core"/"Onyxia's Lair"/"Blackwing Lair"/"Ahn'Qiraj"/"Naxxramas", hp:>60] Repentance
/cast ?[type:boss] Repentance
/cast [mybuff:"Zeal"<#3/"Zeal"<7] Crusader Strike
/cast [mybuff:"Holy Might"<5] Holy Strike
/cast [mypower:>45] Consecration
/cast ?[mypower:<70] Quel'dorei Meditation
/cast [type:undead] Exorcism
/cast [hp:<20] Hammer of Wrath
/cast Crusader Strike
```

```
Example to use trinket slot:
/use 19343(itemID)
```
### Auto Attack - Aoe
**!Only use Quel'dorei Meditation if you are High Elf.**

Stack 3 Zeals, get holy might buff on cooldown, cast consecration while mana above 15%, cast Holy Wrath on cooldown, Hammer of Wrath when available.
```
#showtooltip
/script UIErrorsFrame:Hide()    <-- Only use this if you dont want those spam messages saying "This ability is not ready yet"
/retarget
/startattack
/cast ?[zone:"Ruins of Ahn'Qiraj"/Zul'Gurub/"Molten Core"/"Onyxia's Lair"/"Blackwing Lair"/"Ahn'Qiraj"/"Naxxramas", hp:>60] Repentance
/cast ?[type:boss] Repentance
/cast [mybuff:"Zeal"<#3/"Zeal"<7] Crusader Strike
/cast [mybuff:"Holy Might"<5] Holy Strike
/cast [mypower:>15] Consecration
/cast ?[mypower:<70] Quel'dorei Meditation
/cast [type:undead] Holy Wrath
/cast [hp:<20] Hammer of Wrath
/cast Crusader Strike
```
---
## Seals
### Wisdom Seal
Seal and Judge Wisdom, Reseal and Judge Command while target has JoW.
```
#showtooltip
/retarget
/startattack
/cast [nodebuff:"Judgement of Wisdom"] !Seal of Wisdom
/cast [nocdgcd] Judgement
/cast [nocdgcd] !Seal of Command
/cast Judgement
```
### Light Seal
Seal and Judge Light, Reseal and Judge Command while target has JoL.
```
#showtooltip
/retarget
/startattack
/cast [nodebuff:"Judgement of Light"] !Seal of Light
/cast [nocdgcd] Judgement
/cast [nocdgcd] !Seal of Command
/cast Judgement
```
### Crusader (With Efficiency Variant)
Seal and Judge Crusader, reseal and Judge Command while target has JotC.
```
#showtooltip
/retarget
/startattack
/cast [nodebuff:"Judgement of the Crusader"] !Seal of the Crusader
/cast [nocdgcd] Judgement
/cast [nocdgcd] !Seal of Command
/cast Judgement
```
**Efficency variant (CrusaderEff)**

Make sure your Crusader seal macro is named **"Crusader"**
This will make sure you are not sealing crusader when ur targets are on low health(usually happens when trash clearing) and that even on low mana you will have Command up with **Rank 1** to waste less mana.
```
#showtooltip
/retarget
/startattack
/cast ?[type:boss] {Crusader}
/cast ?[hp:>65, mypower:>40] {Crusader}
/cast [debuff:"Judgement of Wisdom"] !Seal of Command
/cast [nodebuff:"Judgement of Wisdom"] !Seal of Command(Rank 1)
/cast Judgement
```

### Righteousness 
#### Spelladin is dead, stop trying it. >:|

## Consumables

You can increase the list of consumes you want to use, since paladin benefits from both melee and spell power bonus. Make sure to search the itemID in the database and add it.
Right now the buff present on this list are:
- Spirit of Zanza
- Elixir of the Mongoose
- Juju Power(Elixir of the Giants if no Juju Power in inventory)
- Winterfall Firewater(Juju Might if no Winterfall Firewater in inventory)
- R.O.I.D.S
- Dense Sharpening Stone
- Power Mushroom
- Dreamtonic
```
#showtooltip
/use [nomybuff:"Spirit of Zanza"] 20079
/use [nomybuff:"Elixir of the Mongoose"] 13452
/use [nomybuff:"Juju Power"] 12451
/use [nomybuff:"Juju Power"/"Elixir of the Giants"] 9206
/use [nomybuff:"Winterfall Firewater"] 12820
/use [nomybuff:"Winterfall Firewater"/"Juju Might"] 12460
/use [nomybuff:"Rage of Ages"]  8410
/use [nomybuff:"Sharpen Blade V"] 12404
/run PickupInventoryItem(16)
/use [nomybuff:"Well Fed"] 51720
/use [nomybuff:"Dreamtonic"] 61423
```

