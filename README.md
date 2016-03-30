# Vim quick cheatsheet

### General

* `u` - Undo the last command
* `U` - Undo all the changes on a line
* `CTRl + R` - Redo the commands (undo the undo's)
* `p` - Put previously deleted text after the cursor

### Moving between lines

* `j`, `k` - Move the cursor down / up
* `G` - To move to the bottom of the file
* `gg`- To move to the start of the file
* `H` - To move high within the viewport
* `M` - To move middle within the viewport
* `L` - to move low within the viewport
* `Ctrl + u` - To move up (a reasonable amount of lines)
* `Ctrl + d` - To move down (a reasonable amount of lines)

### Moving within a line 

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
* `2w` - To move the cursor two words forward (*you could use a different number*)
* `3e` - To move the cursor to the end of the third word forward

### Insertions

* `O` - To insert a line above the cursor
* `o` - To insert a line below the cursor

### Delete

* `dw` - Delete until the start of the next word
* `de` - Delete to the end of the current word
* `d$` - Delete to the end of the line
* `d2w` - Delete two consecutive words (*you could use a different number*)
* `dd` - Delete the complete line
* `2dd` - Delete two lines (*you could use a different number*)

### Changing existing lines

* `rx`- Use it to replace the character at the cursor with `x`
* `ce` - To change until the end of a word (it'll delete the word and change to Insert mode)
* `c$`- Almost the same as the previous one, but this will delete until the end of the line and then change to Insert mode

### Search

* `/` Searches forward for a phrase
* `?` - Searches backward for a phrase
* `n` - to search for the same word
* `N` - to search for the same word in the opposite direction
* `?` - to search for a phrase in the backward direction
* `%`- For matching parentheses search

### Substituting

* `:s/old/new` - Changes the first ocurrence of "old" for "new"
* `:s/old/new/g`- Changes all the ocurrences of "old" for "new" in a line 
* `:%s/old/new/g` - Changes all the ocurrences of "old" for "new" in a file
* `:%s/old/new/gc` - Changes all the ocurrences of "old" for "new" in a file with a prompt whether to substitute or not
* `:#,#s/old/new/g` - Changes all the ocurrences of "old" for "new" between two lines indicated by `#`

### External Commands

* `:r <file_name>` - Retrives the file name and puts it below the cursor position
* `:r !dir` - Reads the output of the dir command and puts it below the cursor position
* `:! <command>`- Execute an external command, to finish it just press <enter>


