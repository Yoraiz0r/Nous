---
tags: on/obsidian, obsidian/plugin
---

# What is it? 
Dataview is an obsidian plugin that lets you run sql like queries against your data. Very useful for creating automated list of things like in this case, the [[Obsidian Plugins this vault uses]]. 

[View on Github](https://github.com/blacksmithgu/obsidian-dataview)

# How do I use it?
It can be a bit confusing at first. I recommend checking out this introductory tutorial view by [[Nicole van der Hoeven]]: 

<iframe width="560" height="315" src="https://www.youtube.com/embed/JTObSymEvWA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Additional Resources

Feel free to also check out [[Denise Todd]]'s fantastic [Dataview for Beginners](https://denisetodd.medium.com/obsidian-dataview-for-beginners-a-checklist-to-help-fix-your-dataview-queries-11acc57f1e48) Article.

## Cheat sheet
After enabling the plugin, you can make a dataview by using a triple-tick code block starting with type `dataview`, then you input your query in the line below it, such as `list` for all the notes in your obsidian librarry, or  `list from "Path/To/Folder"`

You can also use `table` instead of `list`, to add details use comma delimited list with any data tags that you'd like, for example `table age,eyes,hair from "Path/To/Folder"`

Data tags used for dataview can be written in the metadata like any other metadata type e.g. `age:30`, or with `key::value` anywhere in a note. e.g. `age::30`

You can also use double percentage block to hide info in the middle e.g. `%%secret right after this block%%` %%you found me!%% , this can be used to hide data for dataview in the middle of the document e.g. `%%age:30%%`

> [!TIP] Finding your biggest notes
> If you ever want to find your biggest available note, use this dataview query `LIST FROM "" SORT file.size DESC LIMIT 15`

## Database Folders
You can right click any folder and choose `new database folder` to make an actual table for extensive editing, such as editing existing fields or making new ones. 

If you hit the `+` button at the top right of the table you can add columns to the table by specifying which one, what its type of column should be, and pressing the note button on the right. Columns added will show on a list so you can customize them further.

> [!TIP] Adding dropdown fields
> You can use the "Select" column type to create dropdown fields to use in your data tables, which is convenient for filling things quickly

> [!TIP] Adding image fields
> Using the "Text" type column and inputing a link to an image will preview that image in the column! Useful for icon fields!

> [!TIP] Customize your columns!
> Each column in the data table has its own settings unique to its type, accessible by right-clicking the column's header. Make sure to customize them to your liking!
> 

Right click on columns in the databse folder to adjust their sorting, insert new columns to their left or right, or temporarily hide them.

### Database Folder Settings
You can Open database settings using the gear icon on the top right, from the various settings one useful to change is "Cell Size" to a wide one. 

You can also Select the source of database data, which means you can use a dataview query and customize the contents to your wish and have multiple database folders with different settings or columns, pointing at the same data set. e.g. `from "Project/Tasks" where due and due < date(today)`

[See detailed queries on Github](https://blacksmithgu.github.io/obsidian-dataview/queries/structure/#filter-sort-group-or-limit-results)

## Dataview Javascript queries
Dataview can call javascript mid-document to show specific information, answering questions you may have about your library dynamically. (e.g. how many notes are tagged as 'person') 

To do so, go to Dataview's [[Settings Window]] and enable javascript queries and inline javascript queries. Afterwards, you can input javascript queries anywhere in your notes. The syntax for these queries is "$=" in `code` blocks.

If you enabled the queries, there's this many pages in the the [[Home|Nous]] repository: `$=dv.pages().length`

an example query would be `dv.pages("person")`

You can also refer to fields filled by the current document like "=this.age" inline in sentences if you use code blocks.

### Dataviewjs
You can make full javascript blocks using a dataviewjs code block e.g.
```dataviewjs
console.log("hello")
```

> [!TIP] Seeing what you can work with
> A 'console.log' will show up if you open the [[Electron DevTools]]. (default shortcut `Ctrl+Shift+I`)
> 
> If you print `console.log(this)` you can see all the fields of your current page, which lets you scan for anything you'd like to use!
> 
> Another useful query is `dv.current()` which shows the current file!



