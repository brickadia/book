# Selector

![Selector](images/Selector.png)

The Selector is a tool for selecting many bricks at once. Currently, you can delete many bricks, cut brick selections, copy and paste brick selections from this tool.

## Getting Started
There are a few ways to select bricks with this tool. This includes:
- Clicking a brick with the tool and resizing the selection box with the handles.
- Clicking a brick with the tool, and then Ctrl-clicking another brick to expand the selection box.

For reference, this is what the selection box and its adjustment handles looks like.

![Selector Box](images/selectorbox.png)

You can also adjust the selection box more precisely (under the size of a stud) by holding the **Fine Selection** keybinding.

## Deleting, Cutting, Copying and Pasting Selections
These actions with the selector all use the standard PC keybindings, although there's an additional keybinding to retain ownership when pasting bricks called **Advanced Paste Selection**.

## Default Keybindings

|Action|Keybinding|Functionality|
|---|---|---|
|Copy Selection|Ctrl + C|Copies the selection in the selection box to the clipboard.|
|Paste Selection|Ctrl + V|Pastes the selection that's stored in the clipboard. **Switches to the Placer tool.**|
|Advanced Paste Selection|Ctrl Shift V|Does the same as Paste Selection, but also keeps the ownership of the selection intact.|
|Cut Selection|Ctrl + X|Cuts the selection in the selection box to the clipboard.|
|Delete Selection|Delete|Deletes everything in the selection box.|
|Fine Selection|Left Ctrl|Hold to resize the selection box precisely (under the size of a stud) while dragging the handles.|