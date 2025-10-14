# vault-template
A template for starting an Obsidian vault.

# About This Vault

Making a lasting vault is hard, this template is to help prevent bloat I've experienced before. Some principles I've come to are listed below:

## Structure
1. Assets - Meta, items that help automate vault usage
2. Inbox - Triage, all new notes automatically get placed here
3. Spaces - Isolated concerns regarding tasks
4. Wiki - Flat directory of knowledge pages, utilizing wiki-links

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
HOTKEYS USED
_ w e r t _ _ i _ p
 _ _ d _ g _ j k _ _ _
  _ _ c _ _ _ _ _ _ 
```

## Vault Principles

Ideas that led to the the current structure of this vault.

1.  A vault should be kept as simple as possible

> _Every abstraction is a bet on generality you often won't need._

2. Plug-in's are a _liability_

Shiny things quickly become dull or unmaintained. Plug-ins should be included with caution and with a sound justification. Always consider the implications of how the vault would be affected if the plugin became unavailable.

3. Knowledge and planning are distint types of information

Wiki-like knowledge is sparse and excels in flat structures. Project planning is dense and can managably evolve into dense nested structures as projects grow.

4. Recording information quickly is the most important quality of a vault

Any friction in recording the current thought can prevent you from writing anything at all. Information get's triaged into `inbox/` to enable quick information capture. Filing to the correct location can happen later.

5. Understandable automation

It should be clear what any action an automated step is doing, and a user should feel confident in being able to do the same manually, should something break. Automations (such as hotkeys) should be easily discoverable to the user, and the mental model of the actions should be able to comfortably sit in one's head.  

<!-- This list is long, complicated, and does not sit inside one's head. It needs revision -->

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
