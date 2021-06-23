# Applicator

The Applicator is a tool for applying components to bricks. The tool is compatible with [**Presets**]().

The current default component list includes:

- [Spot Light]()
- [Point Light]()
- [Audio]()
- [Item Spawn]()

## Getting Started

To get started, point at a brick of your choosing and left click with the Applicator tool equipped. The Applicator menu will appear.

![Applicator Menu](images/applicatormenu.png)

When outside the Applicator menu, you can **Ctrl + C** on a brick to copy its properties. Once you have done that, you can **Ctrl + V** to paste those properties on other bricks 

## Brick Properties

**1. Visibility**

Visibility of the brick can be toggled by clicking the switch next to "Visible" in the Applicator menu.

**2. Collision**

Collision can be toggled in 3 levels (in order):

- Player collision
- Projectile collision (bullets, rockets, etc...)
- Interact collision (clicking, etc...)

They can be toggled by clicking the head, gun or hand buttons in the Applicator menu (in order).

## Components

- To add a *component*, click the + button on the right of the Applicator menu.
- To remove a *component*, click the red trash can button on an existing component.
- To edit a *component*, click the "Edit" button on an existing component.

## Probing with the Applicator

The Applicator can also let you view existing components of a brick outside the Applicator menu, as seen in the example below.

![Applicator Menu](images/applicatorprobe.png)

## Default Keybindings

|Action|Keybinding|Functionality|
|---|---|---|
|Copy Properties|Ctrl + C|Copies properties and components from a brick to the clipboard.|
|Paste Properties|Ctrl + V|Pastes properties and components in the clipboard.|