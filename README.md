# Vim like settings for VSCode
- VSCodeVim required
- custom keybinds for terminal, editor, explorer pane navigation

## Files
- [VsCode Settings](settings.json)
- [VsCode Keybinds](keybindings.json)
- [VSCodeVim Keybinds](https://github.com/VSCodeVim/Vim/blob/master/ROADMAP.md)

## Vim Custom keybinds

### General
| Keys       | Description | mode |
| ---------- | ----------- | ---- |
| `<Leader>` | `<Space>`   | -    |

### Vscode
| Keys        | Description           | Mode             |
| ----------- | --------------------- | ---------------- |
| `<Leader>`n | new file              | Normal           |
| `<Leader>`. | quick fix             | Normal           |
| `<Leader>`c | change all occursence | Normal           |
| `<Leader>`f | vscode find           | Normal or Visual |
| >           | vscode indent         | Visual           |
| <           | vscode outdent        | Visual           |

### Vim
| Keys        | Description  | Mode             |
| ----------- | ------------ | ---------------- |
| n           | nzz          | Normal           |
| jj          | `<Esc>`      | Insert           |
| N           | Nzz          | Normal           |
| `<Leader>`o | o`<Esc>`0"_D | Normal           |
| `<Leader>`O | O`<Esc>`0"_D | Normal           |
| `<Leader>`y | "+y          | Normal or Visual |
| `<Leader>`p | "+p          | Normal or Visual |
| p           | pgvy         | Visual           |

## VsCode Custom Keybinds

- `alt` or `option` is the main `trigger` key for most of the bindings
- associate `shift` with `group`
- associate `ctrl` with `move`

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
| Keys  | Description           | Focus   |
| ----- | --------------------- | ------- |
| alt+j | Next sidebar view     | Sidebar |
| alt+k | Previous sidebar view | Sidebar |

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
| Keys        | Description                            | Focus                       |
| ----------- | -------------------------------------- | --------------------------- |
| alt+j       | Next command pallet list               | Command pallete or snippets |
| alt+k       | Previous command pallet list           | Command pallete or snippets |
| j           | List select next (can be any list)     | Any List                    |
| k           | List select previous (can be any list) | Any List                    |
| shift+alt+j | duplicate line down                    | Editor                      |
| shift+alt+k | duplicate line up                      | Editor                      |

### Special keys
| Keys        | Description       | Focus                     |
| ----------- | ----------------- | ------------------------- |
| alt+m alt+d | Maximize terminal | Terminal or terminal tabs |
| alt+m alt+f | Maximize terminal | Terminal or terminal tabs |
| alt+m alt+s | Toggle zen mode   | Any                       |
