---
tags:
  - space/index
---

# Navigation

### Recent Files

```base
views:
  - type: table
    name: Table
    filters:
      not:
        - file.inFolder("spaces/archive")
        - file.inFolder("assets")
    order:
      - file.name
      - file.mtime
      - file.size
    sort:
      - property: file.mtime
        direction: DESC
    limit: 5
    columnSize:
      file.mtime: 290

```

### Inbox
```base
views:
  - type: table
    name: Table
    filters:
      and:
        - file.inFolder("inbox")
```
## Hotkeys

| Shortcut  | Action                                   | Category   |
| --------- | ---------------------------------------- | ---------- |
| Ctrl+N    | Create new file using template           | General    |
| Alt+N     | Create new file without template         | General    |
| Alt+W     | Create new wiki entry                    | General    |
| Alt+Space | Open daily note                          | General    |
| Alt+J     | Go to previous daily note                | General    |
| Alt+K     | Go to next daily note                    | General    |
| Alt+/     | Toggle live preview/source               | Utility    |
| Alt+T     | Insert timestamp at cursor               | Utility    |
| Alt+D     | Insert data at cursor                    | Utility    |
| Alt+X     | Remove empty sections                    | Utility    |
| Alt+R     | Apply templater template in current file | Templater  |
| Alt+I     | Insert template into current file        | Templater  |
| Alt+;     | Insert embed                             | Links      |
| Alt+L     | Insert wiki-link                         | Links      |
| Alt+<     | Show incoming links                      | Links      |
| Alt+>     | Show outgoing links                      | Links      |
| Alt+M     | Open recurring meeting notes             | Navigation |

```
ALT Hotkeys
_ _ _ _ _ _ _ _ _ _ _ _ _
   _ w e r t _ _ i _ _ _ _ _
    _ _ d _ _ _ j k l ; _
     _ _ _ _ _ n m _ _ /
	     space

FULL KEYBOARD
` 1 2 3 4 5 6 7 8 9 0 - =
   q w e r t y u i o p [ ] \
    a s d f g h j k l ; '
     z x c v b n m , . /

```
  

# About This Vault
---
This vault should be kept as simple as possible.

> *Every abstraction is a bet on generality you often won't need.*
## Structure
1. Assets - Meta, files that help automate vault usage
2. Burn - Disposable notes, meant for deletion
3. Inbox - Triage, all new notes automatically get placed here.
4. Spaces - Isolated concerns regarding tasks
5. Wiki - Flat directory of knowledge pages, utilizing wiki-links
## Plugins

> [!warning]
> Plug-ins are a _liability_ not an asset, and should be kept minimal and removed if possible.

| Name                | Justification                      |
| ------------------- | ---------------------------------- |
| Templater           | Dynamic templates                  |
| Terminal            | Quick access to command line tools |
  
