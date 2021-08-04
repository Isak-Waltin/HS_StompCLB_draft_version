# Tecnical Details

How to use the development tools for OTAS

## 2D map creation

To create and edit 2D maps for the game, go to [Awesome_E's Project Builder](https://awesome-e.github.io/hs-tools/hs-builder/), click 'open' and use the UUID "11tigus0le". Play the project and go to the 2D map editor.

* Move the map by scrolling
* Tap a tile to change it to the selected tile type
* To select a tile type, use the arrow buttons in the toolbar (bottom right corner)
* To change the map size, click the text in the toolbar
* To export a map, click the button that says "'Print' Map Data" and copy all the text in the window that pops up
* To load a map, click the button that says "Load Map Data" and paste in map data

As of writing, there are no tile textures. These will have to be created, and the imported. See "Configuring Data" for details.

## Configuring Data

Most of the data and images used in the project can be found in the main scene "Raycaster Engine", in the object "Setup" (looks like a wrench), inside the custom rule "Other Data".

Data that can be modified and added there (non exhaustive):
* 2D map tile textures ("Set Tile Image"). The variable "mem_W1" controls the apparent size of that sprite.
* Dialogues ("Set Dialogue"). Add a new if block and write the dialogue ID as the conditional. "RC_general_data" sets the text in the dialogue, "DialogueCharacterID" will set what character is saying the dialogue (not implemented yet). Optionally, a "Dialogue_NextDialogueID" can be set, if the dialogue should cover more than one "page".

## Command Interpreter

There is a simple command interpreter/terminal in the project. It is in the upper left corner and looks like this: "_/".

Tapping it and entering a command will run that command.

Some useful commands:
| Command | Argument 1 | Argument 2 | Information |
|---|---|---|---|
|roomtp| room index (a number)|| Teleports the player to a room in the raycaster engine|
|dialogue| dialogue index (can be anything, as long as a dialogue exists for that ID)|| Displays a dialogue.|
| set| variable (state, colors, time, door, or mapsize)| value| Sets a variable in the project to a given value|
|run | Message|| Uses the Broadcast Message block to broadcast a Message|
|||||
