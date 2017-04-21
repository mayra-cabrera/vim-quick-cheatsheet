# Vim quick cheatsheet

## General

* `u` - Undo the last command
* `U` - Undo all the changes on a line
* `p` - Put previously deleted text after the cursor
* `v` - To select text, after pressing `v` move the cursor around and then press `:`. You can do whatever you want with the selected course (write `w test` to save it to another file called test or `d` to delete it)

## Moving between lines

* `j`, `k` - Move the cursor down / up
* `G` - To move to the bottom of the file
* `gg`- To move to the start of the file
* `ngg` - Go to given line n
* ```` - Returns you to your original position (after `gg` command).
* `H` - To move high within the viewport
* `M` - To move middle within the viewport
* `L` - To move low within the viewport
* `Ctrl + U` - To move up (a reasonable amount of lines - half screen)
* `Ctrl + D` - To move down (a reasonable amount of lines - half screen)
* `{` - Move to the beginning of current paragraph
* `}` - Move to the beginning of the next paragraph

# Moving within a line 

* `0` - To move to the start of the line
* `h`, `l` - Move the cursor left / right
* `w` - To move foward a word 
* `b` - To move backward a word 
* `e` - To move to the end of the word
* `fx` - Moves the cursor to next ocurrence of x in the line (_x stands for any character_). e.g `f4` will move to the next 4
* `Fx` - Moves cursor to previous ocurrence of x in the line (_x stands for any character_).
* `tx` - Moves cursor to character _before_ next ocurrence of x in the line.
* `Tx` - Moves cursor to character _after_ previous ocurrence of x in the line.
* `;` - Repeat last `f`, `t`, `F` or `T` command
* `,` - Repeat last `f`, `t`, `F` or `T` command but in opposite direction
* `+` - To the first character of the next line (`Enter` does the same thing)
* `-` - To the first character of the previous line

You can use this motions with numbers:
* `2w` - To move forward the cursor two words (*you could use a different number*)
* `3e` - To move forward the cursor to the end of the third word 

## Insertions

* `I` - Insert text at the beginning of the line.
* `O` - To insert a line above the cursor
* `o` - To insert a line below the cursor
* `a` - To insert text after the cursor
* `A` - To insert after the end of the line

You can use this motions with numbers:

* `50i*ESC` - Inserts 50 asterisks
* `25a*-` - Appends 50 characters (25 pairs of asterik and hyphen)

## Deletions

* `dw` - Delete until the start of the next word
* `de` - Delete to the end of the current word.
* `dE` - Delete until the end of the word, including punctuation
* `dH` - Deletes top of the screen
* `d$` - Delete to the end of the line. `D` will also do the trick.
* `dj` - Delete down a line
* `dd` - Delete the complete line
* `dt,` - Delete until `,`, you can use it with another character
* `df,` - Delete before the `,` you can use it with another character
* `daw` - Delete the complete word. It doesn't matter where the cursor is
* `dip` - Deletes the inner paragraph
* `dap` - Deletes a paragraph
* `s` - Delete character at cursor and substitute text
* `S` - Delete line and substitute text

You can user this motions with numbers:

* `d2w` - Delete two consecutive words (*you could use a different number*)
* `d2e` - Delete to the end of the second word 
* `2dd` - Delete two lines (*you could use a different number*)
* `:1,$d` - Deletes all lines in a file

## Changing existing lines

* `rx`- Use it to replace the character at the cursor with `x` (*you could use a different number*)
* `Rx` - Same as before, but this replace more than one character (every typed character deletes an existing one)
* `cw` - Delete until the start of the next word and change you to insert mode
* `ce` - To change until the end of a word (it'll delete the word and change to Insert mode)
* `c$`- Almost the same as the previous one, but this will delete until the end of the line and then change to Insert mode
* `cj` - Deletes down a line and change you to insert mode
* `cc` - Deletes a line and change you into insert mode
* `caw`- Deletes a complete word and change you into insert mode
* `~` - Will change a lowercase letter to uppecase or an uppercase letter to lowercase.
* `cH` - Changes top of the screen

## Joining lines together

* `J` - Merges two lines into one, position the cursor anywhere on the first line.

You can use this motions with numbers:

* `3J` - Joins three consecutve lines.

## Search

* `/` Searches forward for a phrase
* `?` - Searches backward for a phrase
* `n` - To search for the same word
* `N` - To search for the same word in the opposite direction
* `?` - To search for a phrase in the backward direction
* `%`- For matching parentheses search

Using `:set xxx`
* `ic` - Ignores upper/loewr case
* `is` - Show partial matchers
* `hls` - Highlight all matching phrases

Prepend "no" to switch an option off (`:set noic`)

## Substituting

* `:s/old/new` - Changes the first ocurrence of "old" for "new"
* `:s/old/new/g`- Changes all the ocurrences of "old" for "new" in a line 
* `:%s/old/new/g` - Changes all the ocurrences of "old" for "new" in a file
* `:%s/old/new/gc` - Changes all the ocurrences of "old" for "new" in a file with a prompt whether to substitute or not
* `:#,#s/old/new/g` - Changes all the ocurrences of "old" for "new" between two lines indicated by `#`

## Moving within a screen

* `H` - Move to the top line on screen
* `M` - Move to middle line on screen
* `L` - Move to last line on screen

## External Commands

* `:r <file_name>` - Retrieves the file name and puts it below the cursor position
* `:r !dir` - Reads the output of the dir command and puts it below the cursor position
* `:! <command>`- Execute an external command, to finish it just press <enter>

## Copying

* `y` - To copy text, this could be used with hightlighted text after selecting it with visual mode or with another operator `yw`
* `yH` - Copy top of the screen

## Repeat

* `.` - Any time you make the same editing command over and over, you can save time with the repeat command.

## Undo

* `u`- You can undo your last command with this one. It seems the cursor needs not to be on the line where the original edit was made.
* `U` - Undoes all edits on a single line, as long as the cursor remains on that line
* `CTRL - R` - To "redo" an undone operation

## Indentation

* `>` - To indent a line
* `<` - To dedent a line
* `=` - To reformat a line (based on the file identation)
* `>ap` - To indent a inner block
* `=ap` - To reformat a inner block

## Windows & Tabs

* `:new` - Open a new window above the current window
* `:vnew` - Open a new window on the side of the current window
* `:split` - Edit a specified file in new window above the current window
* `:vsplit` - Edit a specified file in new window beside the current window
* `Ctrl + w + (h,j,k,l)` - Navigate to the window in the given direction (h, j, k, l)
* `Ctrl + w + (H, J, K, L)` - Move the current window in the given direction
* `[count] Ctrl + w -` - Decrease the height of the current window
* `[count] Ctrl + w +` - Increase the height of the current window
* `[count] Ctrl + w <` - Decrease the width of the current window
* `[count] Ctrl + w >` - Increase the width of the current window
* `Ctrl + w =` - Equalize the width and height of all windows

## Position the bugger

* `zz` - Center the current line within the window
* `zt` - Bring the current line to the top of the window
* `zb` - Bring the current line to the bottom of the window

## Tabs

* `:tabnew` - Opens a new tab
* `:tabedit` - Edit the specific file in a new tab
* `:gt` - Go to the next tab
* `:GT` - Go to the previous tab
* `Ctrl + w + T` - Break the current window out to a new tab

## Visual Modes

* `V` - Changes to visual line mode which operates on entire lines at a time.
* `Ctrl + v`- Changes to visual block mode which allows you for selecting a column or a text. You can use `I` or `A` to insert text before or after, Vim will only show the change for the first line of the block, but will then replicate to all lines after you complete the change and hit `esc`. Really helpful for `git rebase` operations

## Configuration

* `:e $MYVIMRC` - Open your vimrc fileand allows for quick editing

### Yanking to Named Buffers

* `"a7yy` - Yank next seven lines into a buffer name a (You can replace a with any character). To put the text back use `"aP`, it will put it after the cursor

## Plugins

### CtrlP

* `Ctrl + k` - Move up in the results lists
* `Ctrl + j`- Move down in the results list
* `Ctrl + p` - Cyclce through previous searches
* `Ctrl + n` - Cycle through foward serches
* `Ctrl + t` - Open the highlighted file in a new tab
* `Ctrl + s` - Open the hightighted file in a new split 

### vim-textobj-rubyblock

* `var` - Select around the current ruby block
* `vir` - Select inside the current ruby block 
* `vam` - Select around current ruby method
- `vim` - Select inside current ruby method
- `vaM` - Select around whole class
- `viM` - Select inside current class

This plugin can also be used with delete, change and yank (`dar` - Todo delete arround current ruby block, `cim` - To change inside current ruby method, etc. How awesome is that?)

### Navigating between ruby file

- `gf` - Jumps to highlighted file
- `ctrl + o` - Returns to original file (after `gf`)
- `find` - Make fuzzy search with an argument, under the hood uses `ctrl+d` to autocomplete the search. *This is what `Econtroller`, `Emodel` & `Eview`` commands use* 

## Extras

### Slackcat

- `:%! slackcat -c test -m image.png` - Sends a image.png to `test`channel in slack
- `:%! slackcat -u mayra -m image.png` - Sends image.png to specific user in slack (in this case to `mayra`) 
