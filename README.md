# Vim quick cheatsheet

## General

* `u` - Undo the last command
* `U` - Undo all the changes on a line
* `CTRl + R` - Redo the commands (undo the undo's)
* `p` - Put previously deleted text after the cursor
* `v` - To select text, after pressing `v` move the cursor around and then press `:`. You can do whatever you want with the selected course (write `w test` to save it to another file called test or `d` to delete it)

## Moving between lines

* `j`, `k` - Move the cursor down / up
* `G` - To move to the bottom of the file
* `gg`- To move to the start of the file
* `H` - To move high within the viewport
* `M` - To move middle within the viewport
* `L` - to move low within the viewport
* `Ctrl + u` - To move up (a reasonable amount of lines)
* `Ctrl + d` - To move down (a reasonable amount of lines)

# Moving within a line 

* `0` - To move to the start of the line
* `h`, `l` - Move the cursor left / right
* `w` - To move foward a word 
* `b` - To move backward a word 
* `e` - To move to the end of the word
* `f` - To move for a letter (e.g `f4` will move to the next 4)
* `F` - To move for a character backwards
* `t` - To move until a character (e.g `t,` will move **until** the next comma)
* `T` - To move until a character backwards
* `;` - Repeat last `f`, `t`, `F` or `T` command
* `,` - Repeat last `f`, `t`, `F` or `T` command but in opposite direction

You can use this motions with numbers:
* `2w` - To move forward the cursor two words (*you could use a different number*)
* `3e` - To move forward the cursor to the end of the third word 

## Insertions

* `O` - To insert a line above the cursor
* `o` - To insert a line below the cursor
* `a` - To insert text after the cursor
* `A` - To insert after the end of the line

### Delete

* `dw` - Delete until the start of the next word
* `de` - Delete to the end of the current word
* `d$` - Delete to the end of the line
* `dj` - Delete down a line
* `d2w` - Delete two consecutive words (*you could use a different number*)
* `d2e` - Delete to the end of the second word 
* `dd` - Delete the complete line
* `2dd` - Delete two lines (*you could use a different number*)
* `dt,` - Delete until `,`, you can use it with another character
* `df,` - Delete before the `,` you can use it with another character
* `daw` - Delete the complete word. It doesn't matter where the cursor is
* `dip` - Deletes the inner paragraph
* `dap` - Deletes a paragraph
* `:1,$d` - Deletes all lines in a file

## Changing existing lines

* `rx`- Use it to replace the character at the cursor with `x`
* `Rx` - Same as before, but this replace more than one character (every typed character deletes an existing one)
* `cw` - Delete until the start of the next word and change you to insert mode
* `ce` - To change until the end of a word (it'll delete the word and change to Insert mode)
* `c$`- Almost the same as the previous one, but this will delete until the end of the line and then change to Insert mode
* `cj` - Deletes down a line and change you to insert mode
* `cc` - Deletes a line and change you into insert mode
* `caw`- Deletes a complete word and change you into insert mode

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

## External Commands

* `:r <file_name>` - Retrieves the file name and puts it below the cursor position
* `:r !dir` - Reads the output of the dir command and puts it below the cursor position
* `:! <command>`- Execute an external command, to finish it just press <enter>

## Copying

* `y` - To copy text, this could be used with hightlighted text after selecting it with visual mode or with another operator `yw`)

## Identation

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

## Tabes

* `:tabnew` - Opens a new tab
* `:tabedit` - Edit the specific file in a new tab
* `:gt` - Go to the next tab
* `:GT` - Go to the previous tab
* `Ctrl + w + T` - Break the current window out to a new tab

## Visual Modes

* `V` - Changes to visual line mode which operates on entire lines at a time.
* `Ctrl + v`- Changes to visual block mode which allows you for selecting a column or a text. You can use `I` or `A` to insert text before or after, Vim will only show the change for the first line of the block, but will then replicate to all lines after you complete the change and hit `esc`. Really helpful for `git rebase` operations

## Configuration

* `:e $MYVIMRC` - Open your vimrc fileand allows for quick editing

## Plugins

### CtrlP

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
