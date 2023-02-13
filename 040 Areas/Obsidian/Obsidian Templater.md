---
tags: on/obsidian, obsidian/plugin
---
# What is it?
Templater is an Obsdian plugin that defines a templating language that lets you insert variables and functions results into your notes, as well as execute JavaScript code manipulating those functions.

[View on Github](https://github.com/SilentVoid13/Templater)

# How do I use it?
Start by enabling the plugin and assigning a "Template folder location" in its [[Settings Window]]. 
Then in that folder you can create a template note. Any text you put in that template will be pasted into a file when you choose to insert the template into said file. This is useful if you have a standard header you like some files to have over a span of lines, or if you want to automate some of the contents with scripting.

After you've created a template, go to any file in which you'd like to use it, then, using the [[Quick Switcher]] look for `Templater: Open Insert Template modal` , and a list of your templates will show up. Choosing any of them will pop them into your file. 

## Creation events
Optionally, you should enable "Trigger Templater on new file Creation" in the plugin's [[Settings Window]]. This lets you run automations within the template file as soon as a file is made with that template. 

Creation event code syntax is wrapped by this `<%`contents`%>`. e.g. `<%tp.date.now()%>` (where `tp` stands for templater) (and this is basically javascript at this point)

> [!TIP] Guided Note Creation
> One particularly useful command is `<%tp.file.cursor(indexhere)%>` (where `indexhere` is replaced with numbers e.g. `0`, `1` ,`2`) which moves your cursor to the position. you can pepper this across your note and use a special hotkey to hop between the commands to quickly move across your note and create guides for yourself.
>
> The default hotkey for this "Jump to next cursor position" is [`Alt + Tab`].

> [!TIP] All the commands!
> Here's [Templater's Official Documentation](https://silentvoid13.github.io/Templater/introduction.html). One particularly noteworthy section is the [tp.system](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/system-module.html) commands, with `tp.system.clipboard()` and `tp.system.prompt`!

