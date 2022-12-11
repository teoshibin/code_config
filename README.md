# Vim like settings for VSCode
- VSCodeVim required
- custom keybinds for terminal, editor, explorer pane navigation

## Vim Custom keybinds
```json
    "vim.debug.loggingLevelForConsole": "debug",
    // "vim.useSystemClipboard": true,
    "vim.leader": "<space>",
    "vim.handleKeys": {
        "<C-w>": false,
    },
    "vim.insertModeKeyBindings": [
        // vim specific
        {
            // quick escape
            "before": ["j", "j"],
            "after": ["<Esc>"]
        },
    ],
    "vim.normalModeKeyBindingsNonRecursive": [

        // vscode specific
        {
            // show quick fix
            "before": ["<Leader>", "."],
            "commands": ["editor.action.quickFix"]
        },
        {
            // change all occurence
            "before": ["<Leader>", "c"],
            "commands": ["editor.action.changeAll"]
        },
        {
            // find pop up
            "before": ["<Leader>", "f"],
            "commands": ["actions.find"]
        },

        // vim specific
        {
            // center find next
            "before": ["n"],
            "after": ["n", "z", "z"]
        },
        {
            // center find previous
            "before": ["N"],
            "after": ["N", "z", "z"]
        },
        {
            // newline below
            "before": ["<Leader>", "o"],
            "after": ["o", "<Esc>", "0", "\"", "_", "D"]
        },
        {
            // newline on top
            "before": ["<Leader>", "O"],
            "after": ["O", "<Esc>", "0", "\"", "_", "D"]
        },
        {
            // newline on top
            "before": ["<Leader>", "y"],
            "after": ["\"", "*", "y"]
        },
        {
            // newline on top
            "before": ["<Leader>", "p"],
            "after": ["\"", "*", "p"]
        },
        // {
        //     // delete without copy
        //     "before": ["d"],
        //     "after": ["\"", "_", "d"]
        // },
        // {
        //     // delete to end without copy
        //     "before": ["D"],
        //     "after": ["\"", "_", "D"]
        // },
        // {
        //     // delete line without copy
        //     "before": ["d", "d"],
        //     "after": ["\"", "_", "d", "d"]
        // },
        // {
        //     // change without copy
        //     "before": ["c"],
        //     "after": ["\"", "_", "c"]
        // },
        // {
        //     // change to end without copy
        //     "before": ["C"],
        //     "after": ["\"", "_", "C"]
        // },
        // {
        //     // change line without copy
        //     "before": ["c", "c"],
        //     "after": ["\"", "_", "c", "c" ]
        // },
        // {
        //     // disable highlight
        //     "before": ["<Leader>","n"],
        //     "commands": [":nohl"]
        // },
    ],
    "vim.commandLineModeKeyBindings": [],
    "vim.commandLineModeKeyBindingsNonRecursive": [],
    "vim.visualModeKeyBindings": [],
    "vim.visualModeKeyBindingsNonRecursive": [
        // vscode specific
        {
            // find selected
            "before": ["<Leader>", "f"],
            "commands": ["actions.find"]
        },
        {
            // indent right
            "before": [">"],
            "commands": ["editor.action.indentLines"]
        },
        {
            // indent left
            "before": ["<"],
            "commands": ["editor.action.outdentLines"]
        },
        {
            // newline on top
            "before": ["<Leader>", "y"],
            "after": ["\"", "*", "y"]
        },
        {
            // newline on top
            "before": ["<Leader>", "p"],
            "after": ["\"", "*", "p"]
        },
        {
            // paste on text without copy
            "before": ["p"],
            "after": ["p", "g", "v", "y"]
        }
        // vim specific
        // {
        //     // visual delete without copy
        //     "before": ["d"],
        //     "after": ["\"", "_", "d"]
        // },
        // {
        //     // visual delete end without copy
        //     "before": ["D"],
        //     "after": ["\"", "_", "D"]
        // },
        // {
        //     // visual change without copy
        //     "before": ["c"],
        //     "after": ["\"", "_", "c"]
        // },
        // {
        //     // visual change end without copy
        //     "before": ["C"],
        //     "after": ["\"", "_", "C"]
        // },
    ],
```


## VsCode Custom Keybinds
Why all this customization, the reason is simple, VScodeVim keybinds outside the editor is janky such as `<Leader>` key doesn't work outside the editor and it doesn't support some of the things I use.

- `alt` or `option` is the main `trigger` key for most of the bindings
- navigation associate `shift` with `group`
- navigation associate `ctrl` with `move`

e.g. Focus previous editor tab   
`alt`+`h` = `trigger`+`previous`, trigger previous tab   

e.g. Focus next editor group   
`shift`+`alt`+`l` = `group`+`trigger`+`next`, trigger next group    

e.g. Move tab to next editor group   
`ctrl`+`shift`+`alt`+`l` = `move`+`group`+`trigger`+`next`, trigger move to next group    

e.g. Move tab to the left   
`ctrl`+`alt`+`h` = `move`+`trigger`+`previous`, trigger move to previous tab    

### Main Keybinds
| Keys        | Description                                                   | Focus |
| ----------- | ------------------------------------------------------------- | ----- |
| alt+a       | Toggle sidebar when hidden or focused. Focus when visible     | Any   |
| alt+s       | Focus active editor                                           | Any   |
| alt+d       | Toggle terminal when hidden or focused and focus when visible | Any   |
| alt+f       | Toggle terminal when hidden and focus terminal tabs           | Any   |
| shift+alt+d | Create new terminal                                           | Any   |

### Sidebar
| Keys  | Description                            | Focus                       |
| ----- | -------------------------------------- | --------------------------- |
| alt+j | Next sidebar view                      | Sidebar                     |
| alt+k | Previous sidebar view                  | Sidebar                     |

### Editor Navigation 
| Keys             | Description                       | Focus  |
| ---------------- | --------------------------------- | ------ |
| alt+h            | Focus previous editor tab         | Editor |
| alt+l            | Focus next editor tab             | Editor |
| shift+alt+h      | Focus previous editor group       | Editor |
| shift+alt+l      | Focus next editor group           | Editor |
| ctrl+alt+h       | Move editor tab to left           | Editor |
| ctrl+alt+l       | Move editor tab to right          | Editor |
| ctrl+shift+alt+h | Move editor tab to previous group | Editor |
| ctrl+shift+alt+l | Move editor tab to next group     | Editor |

### Terminal Navigation
| Keys        | Description                      | Focus    |
| ----------- | -------------------------------- | -------- |
| alt+h       | Focus previous splitted terminal | Terminal |
| alt+l       | Focus next splitted terminal     | Terminal |
| shift+alt+h | Focus previous terminal group    | Terminal |
| shift+alt+l | Focus next terminal group        | Terminal |

### Panel Splitting
| Keys        | Description             | Focus         |
| ----------- | ----------------------- | ------------- |
| alt+;       | Split editor right      | Editor        |
| shift+alt+; | Split editor down       | Editor        |
| alt+;       | Split terminal to right | Terminal      |
| alt+;       | Split terminal to right | Terminal tabs |

### Panel Closing
| Keys   | Description    | Focus         |
| ------ | -------------- | ------------- |
| ctrl+w | Close terminal | Terminal      |
| ctrl+w | Close terminal | Terminal tabs |
| ctrl+w | Close editor   | Editor        |

### Panel Size
| Keys  | Description                  | Focus |
| ----- | ---------------------------- | ----- |
| alt+= | Increase focused region size | Any   |
| alt+- | Decrease focused region size | Any   |

### General
| Keys  | Description                            | Focus                       |
| ----- | -------------------------------------- | --------------------------- |
| alt+j | Next command pallet list               | Command pallete or snippets |
| alt+k | Previous command pallet list           | Command pallete or snippets |
| j     | List select next (can be any list)     | Any List                    |
| k     | List select previous (can be any list) | Any List                    |

### Special keys
| Keys        | Description       | Focus                     |
| ----------- | ----------------- | ------------------------- |
| alt+m alt+d | Maximize terminal | Terminal or terminal tabs |
| alt+m alt+f | Maximize terminal | Terminal or terminal tabs |
| alt+m alt+s | Toggle zen mode   | Any                       |