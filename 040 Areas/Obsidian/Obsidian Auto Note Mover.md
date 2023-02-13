---
tags: on/obsidian, obsidian/plugin
---
# What is it?
Auto Note Mover is an obsidian plugin that moves notes to specific folders automatically, once they meet certain criterias - such as tags or regex queries. Useful to organize newly made notes without doing so manually.

# How do I use it?
First, enable the plugin and go to its [[Settings Window]], then add excluded folders to protect any of your special folders in the library. (such as an explicit meta folder and attachments folder, as well as specific plugin assets folders e.g. [[Obsidian Metadata Menu|Metadata Menu's Fileclass folder]] or [[Obsidian Templater|Templater's templates 
folder]])

After you've set your exclusions, add new rules. You can add new rules in the [[Settings Window]], start by choosing a target folder, then matching tags & regex if you need it. Notes given the tag will move to the target folder.

> [!TIP] Understanding file movements
> Movement rules have priorities, the first met rule will be the one used, you can adjust the priority in the plugin's [[Settings Window]]!

