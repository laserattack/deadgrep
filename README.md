# Deadgrep: use ripgrep from Emacs ☠️

Deadgrep is the fast, beautiful text search that your Emacs deserves.

## Usage

### Keybindings

Navigating results:

| Key                               | Action                                         |
| ---                               | ---                                            |
| <kbd>RET</kbd>                    | Visit the result, file or push button at point |
| <kbd>o</kbd>                      | Visit the result in another window             |
| <kbd>n</kbd> and <kbd>p</kbd>     | Move between search hits                       |
| <kbd>M-n</kbd> and <kbd>M-p</kbd> | Move between file headers                      |

The commands `deadgrep-forward` and `deadgrep-backward` are also
available to move between buttons as well as search hits.

Starting/stopping a search:

| Key                           | Action                                                                  |
| ---                           | ---                                                                     |
| <kbd>S</kbd>                  | Change the search term                                                  |
| <kbd>T</kbd>                  | Cycle through available search types: string, words, regexp             |
| <kbd>C</kbd>                  | Cycle through case sensitivity types: smart, sensitive, ignore          |
| <kbd>F</kbd>                  | Cycle through file modes: all, type, glob                               |
| <kbd>I</kbd>                  | Switch to incremental search, re-running on every keystroke             |
| <kbd>D</kbd>                  | Change the search directory                                             |
| <kbd>^</kbd>                  | Re-run the search in the parent directory                               |
| <kbd>g</kbd>                  | Re-run the search                                                       |
| <kbd>TAB</kbd>                | Expand/collapse results for a file                                      |
| <kbd>C-c</kbd> <kbd>C-k</kbd> | Stop a running search                                                   |
| <kbd>C-u</kbd>                | A prefix argument prevents search commands from starting automatically. |

### Additional interactive commands

| Name                        | Action                                                         |
| ---                         | ---                                                            |
| `imenu`                     | Move between files in a results buffer.                        |
| `deadgrep-kill-all-buffers` | Kill all open deadgrep buffers.                                |
| `deadgrep-debug`            | In a results buffer, view the `rg` command, output and environment used. |

### Minibuffer

You use the minibuffer to enter a new search term.

You can also reuse a previous search term with <kbd>M-p</kbd> in the
minibuffer. To edit the default search term, use <kbd>M-n</kbd>.

### Easy Debugging

The easiest way to debug search results is to review the actual `rg` command executed.

Fortunately, the `deadgrep-debug` function makes it easy:

- Move to the deadgrep results buffer.
- Type `M-x deadgrep-debug`.
- Strike `enter`, and the debug buffer will appear.
- Move to the deadgrep debug buffer.

Study the results to review the `rg` command string and other debugging information to assist you.
