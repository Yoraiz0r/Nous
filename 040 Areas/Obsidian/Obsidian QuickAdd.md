---
tags: on/obsidian, obsidian/plugin
---
# What is it?
QuickAdd is an Obsidian plugin that lets you create notes with predefined contents quickly, building upon [[Obsidian Templater|Templater]].  QuickAdd can create brand new notes as well as capture and process content from one note into another existing note, when you want it to.

# How do I use it?
Enable the plugin and then open its [[Settings Window]], you'll have an input field to name a quickadd command and choose its type, near an "Add" button. Command types are described below:
| Command Type | Description |
| ------------ | ----------- |
| Template | makes a note from a template |
| Capture | captures a region and processes it |
| Macro | Lets you run any other command Obsidian and any other plugins that exist in your library have |
| Multi | Creates a folder dropdown for other commands to be added inside (e.g. 'Add' multi rule, with 'Person' template command in it) |

> [!Warning] Putting things in and out of Multi Rules
> While not easy to grasp immediately, you can grab commands in QuickAdd's settings menu on the right of each command, by dragging the burger (3 horizontal lines) icon.
> 
> Likewise, a multi command has to be expanded to accept any items (arrow pointing down on the left of it), and when you drag a command into the multi command, there's only very few pixels to show its going to be accepted inside. Be careful!

After you create a command, it will be findable in the [[Command Palette]]. You can choose to enable searching for it in the [[Quick Switcher]] and adding a hotkey binding for it by pressing the "⚡" button on the right of the command.

## Template commands
Template commands use premade templates such as ones made using [[Obsidian Templater|Templater]] through a quick shortcut. 

You can press the "⚙" gear button on the right of the command to open a prompt to adjust the command's settings, and choose your template path. There's no autocomplete so you have to know your paths.

In the File Name format, you can choose to use double curly brackets to apply special dynamic naming such as including the name to the note or the likes `{{DATE}}`. There's autocomplete for these, so don't be afraid to explore!

You can also choose whether the newly created note will be opened or not. Useful to keep disabled if you're making quick notes to filter later.

> [!TIP] Synergy with other plugins
> Using Template commands with [[Obsidian Auto Note Mover|Auto Note Mover]] is incredibly effective. Specifying a tag in the template and letting the new note be picked up by Auto Note Mover immediately can save a lot of time!



