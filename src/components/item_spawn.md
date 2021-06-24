# Item Spawn

![Icon](../images/components/item_spawn.png)

![Item Spawn Example](../images/components/item_spawn_example.png)

This component can spawn weapons and adjust their pick-up appearance. Compatible with [Minigames]().

![Edit Menu](../images/components/edit_menu_item_spawn.png)

## Basic Settings

* **Pickup** - This determines the spawned item.
* **Allow Pickup** - Whether you can pick up the item or not. If this is off, the item is permanently transparent.
* **Auto Disable** - If this is enabled, this will disable the pick-up when someone picks up the item.
* **Respawn Time** - This determines the waiting time for an item to be able to be picked up.
* **Respawns on Round Start** - This determines if the item can be picked up instantly when a new round starts.
* **Delay After Round Start** - This determines the delay period before you can pick up the item.

## Positioning
* **Offset Direction** - Direction that the item will be shown, relative to the brick.
* **Offset Distance** - Distance between the item itself and the brick with this component.
* **Rotation** - The rotation of the item.
* **Scale** - The scale of the spawned item.

## Animation

Animation is a toggleable property.

* **Animation Axis** - The axis that the item will spin on.
* **Use Relative Axis** - The relative axis that the item will spin on.
* **Spin Speed** - The speed at which the item spins.
* **Bob Speed** - The speed at which the item bobs vertically.
* **Bob Height** - The maximum height of the item's vertical bobbing.
* **Phase** - The phase of the animation.