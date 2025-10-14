# Quickstart

```meta-bind-button
label: Open Daily Note
icon: ""
style: primary
class: ""
cssStyle: ""
backgroundImage: ""
tooltip: ""
id: ""
hidden: false
actions:
  - type: command
    command: daily-notes

```

```meta-bind-button
label: Create Wiki Entry
icon: ""
style: primary
class: ""
cssStyle: ""
backgroundImage: ""
tooltip: ""
id: ""
hidden: false
actions:
  - type: templaterCreateNote
    templateFile: assets/templates/template-wiki.md
    folderPath: inbox
    fileName: ""
    openNote: true
    openIfAlreadyExists: true

```
# Navigation

Recent spaces

## Hotkeys

| Shortcut     | Action                                       |
| ------------ | -------------------------------------------- |
| Alt+I, Alt+E | Apply templater template to current fille    |
| Ctrl+N       | Create new file and choose a template for it |
| Alt+G        | Commit all changes and push                  |
| Alt+W        | Create new wiki entry                        |
| Alt+Space    | Go to daily note                             |
| Alt+J        | Go to next daily note                        |
| Alt+K        | Go to previous daily note                    |
|              | Turn page into wiki (To-do)                  |
| Alt+R        | Apply templater template in-file             |
| Alt+T        | Insert current timestamp                     |
| Alt+D        | Insert current date                          |
| Alt+P        | Git push                                     |
| Alt+C        | Git commit all                               |
```
_ w e r t _ _ i _ p
 _ _ d _ g _ j k _ _ _
  _ _ c _ _ _ _ _ _ 
```


# About This Vault

This vault should be kept as simple as possible

> _Every abstraction is a bet on generality you often won't need._
## Structure
1. Assets - Meta, items that help automate vault usage
2. Inbox - Triage, all new notes automatically get placed here
3. Spaces - Isolated concerns regarding tasks
4. Wiki - Flat directory of knowledge pages, utilizing wiki-links
## Plug-ins

> [!warning]
> Plug-ins are a _liability_, not an asset. They should be kept to minimum when possible.

| Name                | Justification                      |
| ------------------- | ---------------------------------- |
| Homepage            | Load home on start-up              |
| Dataview            | Dynamically create tables          |
| Meta Bind           | Assign commands to buttons         |
| Various Complements | IDE-like wiki-link autocomplete    |
| Templater           | Programmable/interactive templates |
| Git                 | Platform agnostic version control  |
| Quickadd            | Chain together commands as macros  |
