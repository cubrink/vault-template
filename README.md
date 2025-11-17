# vault-template
A template for starting an Obsidian vault.

# About This Vault

Making a lasting vault is hard, this template is to help prevent bloat I've experienced before.

## Structure
1. Assets - Meta, items that help automate vault usage
2. Burn - Transient notes, delete frequently
3. Inbox - Triage, all new notes automatically get placed here
4. Spaces - Isolated concerns regarding tasks
5. Wiki - Flat directory of knowledge pages, utilizing wiki-links

## Hotkeys

| Shortcut  | Action                                   | Category   |
| --------- | ---------------------------------------- | ---------- |
| Ctrl+N    | Create new file using template           | General    |
| Alt+N     | Create new file without template         | General    |
| Alt+W     | Create new wiki entry                    | General    |
| Alt+M     | Open recurring meeting notes             | Navigation |
| Alt+Space | Open daily note                          | Navigation |
| Alt+J     | Go to previous daily note                | Navigation |
| Alt+K     | Go to next daily note                    | Navigation |
| Alt+;     | Insert embed                             | Links      |
| Alt+L     | Insert wiki-link                         | Links      |
| Alt+<     | Show incoming links                      | Links      |
| Alt+>     | Show outgoing links                      | Links      |
| Alt+R     | Apply templater template in current file | Templater  |
| Alt+I     | Insert template into current file        | Templater  |
| Alt+/     | Toggle live preview/source               | Utility    |
| Alt+T     | Insert timestamp at cursor               | Utility    |
| Alt+D     | Insert data at cursor                    | Utility    |
| Alt+X     | Remove empty sections                    | Utility    |

```
ALT Hotkeys
_ _ _ _ _ _ _ _ _ _ _ _ _
   _ w e r t _ _ i _ _ _ _ _
    _ _ d _ _ _ j k l ; _
     _ x _ _ _ n m _ _ /
	     space

FULL KEYBOARD
` 1 2 3 4 5 6 7 8 9 0 - =
   q w e r t y u i o p [ ] \
    a s d f g h j k l ; '
     z x c v b n m , . /

```

## Vault Principles

Ideas that led to the the current structure of this vault.

1.  A vault should be kept as simple as possible

> _Every abstraction is a bet on generality you often won't need._

2. Plug-in's are a _liability_

Shiny things quickly become dull or unmaintained. Plug-ins should be included with caution and with a sound justification. Always consider the implications of how the vault would be affected if the plugin became unavailable.

3. Knowledge and planning are distinct types of information

Wiki-like knowledge is sparse and excels in flat structures. Project planning is dense and can managably evolve into dense nested structures as projects grow.

4. Recording information quickly is the most important quality of a vault

Any friction in recording the current thought can prevent you from writing anything at all. Information get's triaged into `inbox/` to enable quick information capture. Filing to the correct location can happen later.

5. Understandable automation

It should be clear what any action an automated step is doing, and a user should feel confident in being able to do the same manually should something break. Automations (such as hotkeys) should be easily discoverable to the user, and the mental model of the actions should be able to comfortably sit in one's head.  

<!-- This list is long, complicated, and does not sit inside one's head. It needs revision -->

## Plugins

> [!warning]
> Plug-ins are a _liability_ not an asset, and should be kept minimal and removed if possible.

| Name                | Justification                      |
| ------------------- | ---------------------------------- |
| Templater           | Dynamic templates                  |
| Terminal            | Quick access to command line tools |
  
