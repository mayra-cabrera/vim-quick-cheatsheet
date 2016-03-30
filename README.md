# Vim quick cheatsheet

### Move the cursor 

* `j`, `k` - Move the cursor down / up
* `h`, `l` - Move the cursor left / right

### General

* `u` - Undo the last command
* `U` - Undo all the changes on a line
* `CTRl + R` - Redo the commands (undo the undo's)
* `p` - Put previously deleted text after the cursor
* `rx`- Use it to replace the character at the cursor with `x`
* `ce` - To change until the end of a word (it'll delete the word and change to Insert mode)
* `c$`- Almost the same as the previous one, but this will delete until the end of the line and then change to Insert mode
* `G` - To move to the bottom of the file
* `gg`- To move to the start of the file
* `o` - To insert a line below the cursor
* `O` - To insert a line above the cursor

### Delete

* `dw` - Delete until the start of the next word
* `de` - Delete to the end of the current word
* `d$` - Delete to the end of the line
* `d2w` - Delete two consecutive words (*you could use a different number*)
* `dd` - Delete the complete line
* `2dd` - Delete two lines (*you could use a different number*)

### Count & Motions

* `2w` - To move the cursor two words forward (*you could use a different number*)
* `3e` - To move the cursor to the end of the third word forward
* `0` - To move to the start of the line

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


