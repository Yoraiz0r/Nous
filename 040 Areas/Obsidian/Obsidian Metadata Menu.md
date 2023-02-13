---
tags: on/obsidian, obsidian/plugin
---
# What is it?
Metadata Menu is an obsidian plugin that adds context menu commands related to metadata, letting you change tags and their information globally and easily.

[View on Github](https://github.com/mdelobelle/metadatamenu)

# How do I use it?
Metadata menu does a lot, I recommend looking at the [full documentation](https://mdelobelle.github.io/metadatamenu/)

## FileClass
Metadata menu introduces a concept of 'fileclass', named tags that have a file defining what other tags should be alongside them. e.g. a `person` should have `age` and `hair`. Introducing FileClasses lets you keep consistency among notes of the same type.

To begin using fileclasses, first go to the plugin's [[Settings Window]] and expand the "FileClass settings" and assign a "class Files path". 

Afterwards, If you go to an existing document and open the dropdown menu on the top right, you can select 'Add a new fileClass'. This will open a prompt to create a new fileClass as well as giving it aliases. 

> [!Bug]
> After making a new file class, changes won't show until you reopen Obsidian!

After assigning a newly created fileclass tag to a note (e.g. adding a `tag: person` to a person note after having made its fileclass), an icon should appear near its name display in various places.
- The explorer panel.
- The header of the file when it is open.
- Whenever the file is linked. 

Clicking that icon will open a window prompt named 'Fields of filename'. Here you can see the fileclasses assigned to the file, and what fields they add, as well as edit them. 
> [!TIP] 
> There's also a useful 'insert missing fields' window pertaining to the specific note you look at, if it is missing any.

> [!TIP] Disabling the metadata menu button in places
> You may that metadata menu's icon creeps its way into almost every visible point in the project. In case you'd like to disable some of those appearances, you can do so in its [[Settings Window]] under the "Metadata Menu Button" collapsible section.

