# NOTE
Please download from 'releases' on the right hand side.

Complete overhaul of weapon parts and jamming.

# Motivation
Weapons dropping at 7% makes no sense. Weapon condition is now treated as general cleanliness and not holistic weapon quality. Weapon part condition represents amount of wear and tear on that part, affecting its performance more than cleanliness. While good quality weapons will be easier to maintain, crappy weapons with crappy parts will be less usable than they are now.

# Major Features

This is the meaty stuff. For an easier start guide, consult Maintenance Guide. You can also read the in-game PDA guide.

## Condition overhaul
- Weapons drop at higher condition from stalkers. This does not mean they are more usable.
- Weapon parts are no longer tied to condition. Weapon jamming from low condition will still happen, and additionally different types of jams from poor-condition parts will occur.
- Overall weapon condition is now interpreted as 'cleanliness' of the weapon - the degree of dirtiness and fouling that has built up.
- Weapons degrade faster in rain (configurable via MCM).
- Keeping weapons in good condition is easier in general. Cleaning tools are much more effective and have more uses.
- Mechanic repair is cheaper - you're only cleaning the weapon (Configurable with MCM).

## Technician changes (PLEASE READ)

- Technicians have three levels of service, configurable in MCM.
- Clean Weapon Only restores weapon condition and no parts.
- Clean Parts restores weapon parts if they are above 60%.
- Full service completely fixes weapons and parts, but is the most expensive.
- Technicians have random parts in stock. The amount increases with toolkits turned in.

## Parts overhaul
- Weapon parts are now a separate subsystem to manage.
- Weapon part condition plays a big role in weapon performance. For now, only two things are affected - weapon jam chance and damage.
- Weapon parts are MUCH easier to replace. Parts replacement requires only clicking and dragging parts onto guns.
- Field replacement of parts will reduce weapon condition. This is reduced if you have a Leatherman. This represents loss of lubrication or introduction of outside material from field replacement.
- Replacing parts with a toolkit at a workbench does not consume charges. Installing upgrades still does.
- Parts are harder to repair. Parts can only be restored from 60% condition with ordinary tools. Otherwise you can purchase a new and expensive toolkit from technicians.
- Parts can be maintained with cleaning and repair kits. There is a right-click menu exposed that will present the available parts to be maintained or replaced.

## Field stripping
- Weapons with parts can be field stripped.
- Field stripping allows removal of parts that can be reasonably removed.
- By default, barrels cannot be replaced. This can be modified in MCM and optionally triggers can be subject to the same restriction.
- Weapons with missing parts will be unable to fire, obviously.
- Parts can be replaced in a field stripped gun either at workbench or with drag and drop like normal.

## Internal damage
- Weapons under 85% condition can suffer internal parts damage with use, rolling per shot to damage one part. 
- The worse condition the weapon, the greater the chance. 
- Reliability upgrades affect the chance of internal damage, so more reliable weapons will damage their parts less than more finicky weapons (AKs will damage their parts far less than SVDs). Keep your weapons as clean as possible.

# Weapon Malfunctions

The vanilla weapon jams have been overhauled into a new, more complicated system. Most of the time this will boil down to a single separate key press to address.

To not confuse the player, jammed weapons cannot be reloaded.
Double tap your `use` key to unjam by default.

Custom jam keys can be set in MCM.
You can also unjam weapons from inventory through right click.
There are three additional types of weapon failure:
1. Misfires. Misfires are a failure of the trigger components and prevent a shot from being fired.
2. Type 1 malfunctions, analogous to failure to eject. The shot is fired but mechanical failure prevents the next shot from loading and/or firing.
3. Type 2 malfunctions, analogous to double-feed. Similar to type 1, but requires unloading the magazine to properly clear the malfunction. Can disable completely with MCM.
The jam chance can be adjusted through MCM.
In addition, barrel damage will reduce gun damage if the barrel condition is below 80%, up to a 50% reduction at 0% condition barrel.

Only weapons with parts will suffer these failures. Gauss Rifle, Armsel Protecta, and P90 lack parts so they do not suffer parts-related failures.

Quick guide to addressing jams:
1. Note the type of jam you have.
2. Press the unjam button.
3. If your weapon is severely jammed, unload your weapon from the inventory. Press the unjam button.

Barrel quality affects damage dealt, because modifying dispersion dynamically is not possible.
Barrels below 75% condition will lose damage up to 50% less damage at 0% condition.

Compatible with MCM. If MCM is not installed, variables can be tweaked in arti_jamming_mcm.

## Changelog
### 1.13.2
- Removed dependency on OPO patch and item_repair.ltx with new repair modifier system.
- Changes to price and uses of weapon repair items have been reverted.
- Repair items have been reworked appropriately. Solvents and sprays can be used from 25% condition but are half as effective below certain thresholds.
- Simplified sale logic to be less restrictive.
### 1.13.1
- Small tweaks for 1.5.2 support (implicit)
- Classic jams now dovetail into the new jams
- Changed how unjams work to prevent soft locks
- Nativized unjam keybind. Still defaults to doubletap use without MCM.
### 1.13
- Removed overheating for now. Will be reworked in the future.
- Weapons now belong to families. Custom parameters for most aspects of a weapon can be customized using the new family system. Default behavior resembles that of previous versions of WPO.
- Barrel replacement in the field is now toggleable. Triggers can now optionally require kits to replace. The misfire chance has been dropped globally and doesn't scale with condition, unlike ordinary jams.

Credits: 

Arszi for help and ideas

Michiko for providing unjam sounds

TDLemon/Aonestr for RUS translate
