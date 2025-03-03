# Prot Paladin Macros
### Make sure you have [CleveRoidMacros](https://github.com/bhhandley/CleveRoidMacros)(Custom functions) and [SuperMacro](https://github.com/Monteo/SuperMacro)(Size extender) installed as they are needed to work.
#### This are the macros I am currently using, feel free to change them as you like as this should be used as a start up to make your ones. If you have any questions, message me on discord @unlifed.
## Index
 1. [Rotations](#rotations)
 2. [Seals](#seals)
 3. [Consumables](#consumables)

## Rotations
### Max threat
```
#showtooltip
/cast [nomybuff:"Righteous Fury"] Righteous Fury
/retarget
/startattack
/cast [nocdgcd]Holy Shield
/cast [nocdgcd,cdgcd:"Holy Shield">1]Holy Strike
/cast [nocdgcd,cdgcd:"Holy Shield">1]Consecration
/cast [type:undead,nocdgcd] Exorcism
```
### Powerfull Self Cleanse 

This will bubble and unbubble you so you clean debuffs that can't be decursed.(needs to be spammed/will put DS on 5min cd)
```
/cast Divine Shield
/unbuff Divine Shield
/retarget
/startattack
```

## Seals | Seal Priority -> Wisdom,Light,Crusader
### Wisdom + Righteousness

Judge Wisdom, Seal and Judge Righteousness on cooldown
```
#showtooltip
/retarget
/startattack
/cast [nodebuff:"Judgement of Wisdom"] !Seal of Wisdom
/cast [nocdgcd] Judgement
/cast [nocdgcd] !Seal of Righteousness
/cast Judgement
```
### Mana

Seal and Judge Wisdom, Reseal Wisdom and keep it up for fast mana recovery
```
#showtooltip
/retarget
/startattack
/cast [nodebuff:"Judgement of Wisdom"] !Seal of Wisdom
/cast [nodebuff:"Judgement of Wisdom"] Judgement
/cast !Seal of Wisdom
```
### Light + Righteousness
```
#showtooltip
/retarget
/startattack
/cast [nodebuff:"Judgement of Light"] !Seal of Light
/cast [nocdgcd] Judgement
/cast [nocdgcd] !Seal of Righteousness
/cast Judgement
```

## Comsumables
WIP