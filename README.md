# W3Redux: Realtime Gamepad Controls

# ARCHIVED: Replaced By: [Realtime Gamepad Controls Next Gen](https://github.com/adam-sunderman/realtime-gamepad-controls)

---

Version: 1.0.1  
Author: Adam Sunderman  
[Official Nexus Mod Page](https://www.nexusmods.com/witcher3/mods/2116/)  
[W3ReduxRGC Git Project](https://github.com/adam-sunderman/modW3ReduxRGC)  
[Video Demo Feature Walkthrough](https://www.youtube.com/watch?v=Lbc-3TxHNaM)

---
## General Notes
Realtime Gamepad Controls is only of use to you if you use an XInput controller. This mod will not be compatible with mouse and keyboard players for general play. The purpose of this mod is to allow for controller players to eliminate the need for the radial menu entirely and attempts to map your equipment inventory as well as all signs in a way that has everything accessible in real time. This mod is self-inclusive and does not require the use of extra software like XPadder or AntiMicro. This mod has not had any localization work done and presents any strings that it shows in ui layers in English translations (hard coded).

## Controls
This mode completely removes the radial menu as it has a focus on **100% realtime controls** in combat. The radial 
menu button (*Left Bumper*) is now the *"Sign/QuickSelect"* Modifier. When you press LB you will notice that your 
quick use item info display will change to show your quick slot items and bombs. These can be toggled and 
selected just like potions as long as the modifier is held. While the *Left Bumper* is held down:  

	LB + X: cast igni (hold for alternate)
	LB + Y: cast aard (hold for alternate)
	LB + B: cast quen (hold for alternate)
	LB + A: cast yrden (hold for alternate)
	LB + RB: cast axii (hold for alternate)
	LB + Dpad Up: select slotted quick use (RB to use)
	LB + Dpad Down: select slotted bomb (RB to throw)
	LB + (Hold) Dpad Up: swap slotted quick use. auto equips (RB to use)
	LB + (Hold) Dpad Down: swap slotted bomb. auto equips (RB to throw)

The cross bow is now mapped to the Right Trigger and is not considered an item anymore. I.E. When you have a 
bomb equipped, fire your crossbow, the bomb is still equipped and RB will still throw it without having to 
re-equip.

All other controls have stayed the same.

With that in mind, if you have any mods that modified input.settings in Documents/Witcher 3/ It would 
definitely be beneficial to start that file fresh as well. This can be accomplished via deleting input.settings 
and starting up witcher 3 and a new one will be generated for you.

## Installation Considerations
This mod makes heavy use of modifying input.settings. Other mods that make additions to this file will be at risk to be harder merges. Particularly of note, this mod intends to heavily modify the behavior of:  

- LB
- RB
- RT
- A
- X
- Y
- B

you will have to be very careful with other mods that attempt to do anything special with these inputs. However, a mod like FriendlyMeditation that alter what clicking the right thumbstick does will not cause much hassle.

This mod makes heavy edits to playerInput.ws and when merging with other mods, this is the file where I do the most manual work. In my experience, script merger is close, but you really have to understand a bit of what both conflicting mods are trying to accomplish to get a successful merge that really is firing on all cylinders. I have merged with FriendlyHUD, Preparations, and ImmersiveCAM without any noticeable issues (along with many other small and simple mods).

##Installation Instructions:
Note: if you are using simple mods and not any overhaul mods (especially if they alter controls), it is more than likely safe to skip steps 1-3

1. Recommended: Backup existing mods and input.settings
2. Recommended: Clear your mods folder and delete your input.settings.
3. Recommended: Start Witcher 3 to generate a new input.settings file.
4. Required: Move the folder containing this file to the mods folder in your Witcher 3 install location
	- example: *{W3InstallLocation}/mods/modRealtimeGamepadControls*
2. Required: Copy all contents from input.settings.begin.txt and paste at the beginning of input.settings in your *'Documents/Witcher 3'* folder
3. Optional: If you are going to start out with other mods already installed, use a tool like WitcherScriptMerger to handle any conflicts.

You are ready to never need to open that lame radial menu again **:D**

#### Alternatively,

For an easier installation, I can fully recommend installation with [Witcher 3 Mod Manager](https://rd.nexusmods.com/witcher3/mods/2678) by [stefan3372](https://rd.nexusmods.com/witcher3/users/42512255). It has proven very successful at installing in my testing. However, as it is helping you bind keys (which it will do automatically) it will notice duplicate entries for *CastSignHold*. You will have to choose to "save all" repeatedly. If you don't save all bindings for this action, you will not be able to alternate cast all 5 signs. Another consideration is on uninstall with Witcher 3 Mod Manager, I have noticed that keybindings stay in the input settings. Not a big deal immediately, but having those left over for future installs could lead to future issues.

## Features
1. Instant Sign Casting via "Sign/QuickSelect" Modifier Button 
2. Instant Quick Selecting of bombs and quick use items via "Sign/QuickSelect" Modifier button 
3. Remapped Crossbow to Right Trigger. Crossbow and other items are now completely separated logically.  
	- Note: Use Item is still Right Bumper
2. Updated Item Info UI to show last used item (not crossbow). So if you were using a bomb, clicked right trigger to fire a crossbow bolt, the selected item according to the UI is still the bomb. This is to really solidify that the crossbow is not an item.
3. Updated Item Info UI to show bombs and quick use items instead of potions while "Sign/QuickSelect" Modifier button is pressed.
4. Added equip sounds while changing which bombs and quick use items you are using
5. Made the quick use potions (and new bombs/items) a lot smarter. If you use your last bomb or potion and your backup slot has charges, The backup with auto equip
6. Updated Button Prompts UI to show available signs while "Sign/QuickSelect" Modifier is pressed while in combat.

## Change Log:
	1.0.1: HOT FIX: fixed issue where alternate cast of Igni and Aard could be prevented from working with Whirl and Aard unlocked
	1.0.0: Officially out of beta. Known high priority bugs resolved and features are ready for official release

## Contribution
This code is going to go up on GitHub for version control ASAP. Any modder is free to fork and make changes as they see fit. If a modder is wanting to distribute their work I only ask that if it is fixing bugs related to the mods original vision, please do a pull request and lets merge it back in. If you used these ideas as a base for your own mods and went in your own direction. Feel free to distribute your mod with source you got from this mod and just credit me. No need to ask me directly. I don't know anything about localizing and if anyone feels like localizing the few UI tweaks in this mod, I would appreciate that.
