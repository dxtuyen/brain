# Vim Cheat Sheet

## 1. Modes

| Key        | Action                                        |
| ---------- | --------------------------------------------- |
| `Esc`      | Return to Normal mode                         |
| `i`        | Insert before cursor                          |
| `a`        | Insert after cursor                           |
| `o`        | Create a new line below and enter Insert mode |
| `O`        | Create a new line above and enter Insert mode |
| `v`        | Enter Visual mode (character selection)       |
| `V`        | Enter Visual Line mode                        |
| `Ctrl + v` | Enter Visual Block mode                       |


## 2. Navigation

### Basic movement

| Key | Action                                                   |
| --- | -------------------------------------------------------- |
| `h` | Move left                                                |
| `j` | Move down                                                |
| `k` | Move up                                                  |
| `l` | Move right                                               |
| `w` | Move to the beginning of the next word                   |
| `b` | Move to the beginning of the previous word               |
| `e` | Move to the end of the word                              |
| `W` | Move to the beginning of the next WORD (space-delimited) |
| `B` | Move to the beginning of the previous WORD               |
| `E` | Move to the end of the WORD                              |

### Line navigation

| Key        | Action                                     |
| ---------- | ------------------------------------------ |
| `0`        | Move to the absolute beginning of the line |
| `^`        | Move to the first non-whitespace character |
| `$`        | Move to the end of the line                |
| `g_`       | Move to the last non-whitespace character  |
| `gg`       | Move to the first line of the file         |
| `G`        | Move to the last line of the file          |
| `nG`       | Move to line `n` (e.g. `20G`)              |
| `:{n}`     | Move to line `n` (e.g. `:20`)              |
| `Ctrl + d` | Scroll down half a screen                  |
| `Ctrl + u` | Scroll up half a screen                    |
| `Ctrl + f` | Scroll forward one screen                  |
| `Ctrl + b` | Scroll backward one screen                 |
| `%`        | Jump to the matching bracket               |

| Key  | Action                                       |
| ---- | -------------------------------------------- |
| `i`  | Insert before cursor                         |
| `a`  | Append after cursor                          |
| `I`  | Insert at the first non-whitespace character |
| `A`  | Append at the end of the line                |
| `o`  | Open a line below                            |
| `O`  | Open a line above                            |
| `r`  | Replace one character                        |
| `R`  | Enter Replace mode                           |
| `s`  | Delete one character and enter Insert mode   |
| `S`  | Replace the entire line                      |
| `cc` | Change the entire line                       |
| `C`  | Change from cursor to end of line            |

| Key   | Action                                       |
| ----- | -------------------------------------------- |
| `x`   | Delete character under cursor                |
| `X`   | Delete character before cursor               |
| `dd`  | Delete the current line                      |
| `D`   | Delete from cursor to end of line            |
| `dw`  | Delete from cursor to the next word boundary |
| `de`  | Delete through the end of the word           |
| `db`  | Delete backward to the beginning of the word |
| `diw` | Delete the word under cursor                 |
| `di"` | Delete text inside double quotes             |
| `di(` | Delete text inside parentheses               |
| `di{` | Delete text inside braces                    |
| `dG`  | Delete from current line to end of file      |

| Key        | Action                                        |
| ---------- | --------------------------------------------- |
| `yy`       | Copy (yank) the current line                  |
| `nyy`      | Copy `n` lines                                |
| `yw`       | Yank from cursor to the next word boundary    |
| `yiw`      | Copy the word under cursor                    |
| `p`        | Paste after cursor or below the current line  |
| `P`        | Paste before cursor or above the current line |
| `dd`       | Delete a line (also stores it in a register)  |
| `u`        | Undo the last change                          |
| `Ctrl + r` | Redo                                          |
| `.`        | Repeat the last change                        |
|            |                                               |

Vim commands can be combined:

- `d` = delete
    
- `c` = change (delete and enter Insert mode)
    
- `y` = yank (copy)
    
- `i` = inside a text object
    
- `a` = around a text object
    

| Command | Action                                |
| ------- | ------------------------------------- |
| `dw`    | Delete to the next word boundary      |
| `d$`    | Delete to end of line                 |
| `d0`    | Delete to beginning of line           |
| `cw`    | Change to the next word boundary      |
| `ciw`   | Change the entire word under cursor   |
| `diw`   | Delete the entire word under cursor   |
| `ci"`   | Change text inside double quotes      |
| `ca"`   | Change text including double quotes   |
| `ci(`   | Change text inside parentheses        |
| `da(`   | Delete parentheses and their contents |
| `ci{`   | Change text inside braces             |
| `cit`   | Change text inside an HTML/XML tag    |
| `dd`    | Delete the entire line                |
| `cc`    | Change the entire line                |
| `yy`    | Copy the entire line                  |
| `3dd`   | Delete three lines                    |
| `5j`    | Move down five lines                  |
| `dG`    | Delete to end of file                 |

## 5. Search and Replace

| Key / Command    | Action                                    |
| ---------------- | ----------------------------------------- |
| `/pattern`       | Search forward                            |
| `?pattern`       | Search backward                           |
| `n`              | Go to the next match                      |
| `N`              | Go to the previous match                  |
| `*`              | Search forward for the word under cursor  |
| `#`              | Search backward for the word under cursor |
| `:noh`           | Clear search highlighting                 |
| `:%s/old/new/g`  | Replace all occurrences in the file       |
| `:%s/old/new/gc` | Replace all occurrences with confirmation |
| `:s/old/new/g`   | Replace occurrences on the current line   |

## 6. Saving and Quitting

| Command       | Action                      |
| ------------- | --------------------------- |
| `:w`          | Save the file               |
| `:w filename` | Save as another filename    |
| `:q`          | Quit                        |
| `:wq`         | Save and quit               |
| `:x`          | Save if modified and quit   |
| `ZZ`          | Save if modified and quit   |
| `:q!`         | Quit without saving changes |
| `ZQ`          | Quit without saving         |

## 7. Files and Buffers

| Command                    | Action                                      |
| -------------------------- | ------------------------------------------- |
| `:e filename`              | Open a file                                 |
| `:e!`                      | Reload the current file, discarding changes |
| `:ls`                      | List buffers                                |
| `:bn`                      | Switch to the next buffer                   |
| `:bp`                      | Switch to the previous buffer               |
| `:b {n}`                   | Switch to buffer number `n`                 |
| `:bd`                      | Delete (close) the current buffer           |
| `:sp filename`             | Open a file in a horizontal split           |
| `:vsp filename`            | Open a file in a vertical split             |
| `Ctrl + w`, then `h/j/k/l` | Move between split windows                  |
| `Ctrl + w`, then `q`       | Close the current split window              |

## 8. Visual Mode

| Key        | Action                          |
| ---------- | ------------------------------- |
| `v`        | Select characters               |
| `V`        | Select whole lines              |
| `Ctrl + v` | Select a rectangular block      |
| `d`        | Delete selection                |
| `y`        | Copy selection                  |
| `c`        | Change selection                |
| `>`        | Indent selection                |
| `<`        | Unindent selection              |
| `gv`       | Reselect the previous selection |
| `Esc`      | Exit Visual mode                |

## 9. Indentation and Formatting

| Key / Command         | Action                       |
| --------------------- | ---------------------------- |
| `>>`                  | Indent the current line      |
| `<<`                  | Unindent the current line    |
| `==`                  | Auto-indent the current line |
| `n>>`                 | Indent `n` lines             |
| `gg=G`                | Re-indent the entire file    |
| `:set number`         | Show line numbers            |
| `:set nonumber`       | Hide line numbers            |
| `:set relativenumber` | Show relative line numbers   |
| `:set nowrap`         | Disable line wrapping        |
| `:set wrap`           | Enable line wrapping         |

## 10. Macros and Registers

|Key / Command|Action|
|---|---|
|`qa`|Start recording a macro into register `a`|
|`q`|Stop recording the macro|
|`@a`|Execute macro `a`|
|`@@`|Repeat the last executed macro|
|`5@a`|Execute macro `a` five times|
|`:reg`|Display registers|
|`"ayy`|Copy the current line into register `a`|
|`"ap`|Paste from register `a`|

## 11. Counts and Command Patterns

Vim lets you combine a count, an operator, and a motion.

**General pattern:**

`[count] + operator + motion`

| Command |Action|
|---|---|
| `3w`    |Move forward three words|
| `5j`    |Move down five lines|
| `3dd`   |Delete three lines|
| `2dw`   |Delete two word motions|
| `d3w`   |Delete across three word motions|
| `c$`    |Change to the end of the line|
| y3j`    |Yank the current line and the next three lines|

## 12. Recommended Learning Order

1. **Navigation:** `w`, `b`, `e`, `0`, `^`, `$`, `gg`, `G`.
    
2. **Basic editing:** `i`, `a`, `o`, `x`, `dd`, `yy`, `p`, `u`.
    
3. **Text objects:** `ciw`, `diw`, `ci"`, `ci(`, `ci{`.
    
4. **Search:** `/`, `n`, `N`, `*`.
    
5. **File management:** `:w`, `:q`, `:wq`, `:e`, `:bn`, `:bp`.
    
6. **Advanced editing:** Visual mode, registers, macros, splits.
    

**Daily workflow:** Navigate → Search → Edit → Save (`:w`) → Continue.

**Remember:** In Normal mode, commands can be combined. For example, `ciw` changes a word, `dd` deletes a line, and `.` repeats the last change.


|     |     |
| --- | --- |
|     |     |
test heleli,ffasfd