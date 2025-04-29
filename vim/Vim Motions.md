**Moving Cursor**
`h,j,k,l`: move cursor  
`4k`: example jump up 4 lines. works with `h,j,k,l`  
`CTRL+u/d`: move cursor half a screen up/down  
`CTRL+b/f`: move full screen up/down  
`zt`: move cursor to top of screen  
`zb`: move cursor to bottom of screen  
`M`: jump to middle of screen  
`^` or `_`: jump to first character of line
`-`: jump to first non-whitespace of previous line  
`+`: jump to first non-whitespace of next line  
`0`: jump to start of line  
`$`: jump to end of line  
`w`: jump one word forward  
`W`: jump one word forward including non-whitespace  
`b`: jump one word backwards  
`B`: jump one word backwards including non-whitespace  
`e`: jump to end of word  
`fx`: jump to next occurrence of character x in line   
`tx`: jump to before next occurrence of character x in line  
`Fx`: jump to the previous occurrence of character x  
`Tx`: jump to after previous occurrence of character x  
`;` : repeat previous f, t, F or T movement  
`,`: repeat previous f, t, F or T movement, backwards  
`ge`: jump backwards to the end of a word  
`gE`: jump backwards to the end of a word including punctuation  
`%`: jump to to matching character (default supported pairs: '()', '{}', '[]'  
`)`: jump to next sentence  
`(`: jump to previous sentence  
`}`: jump to next paragraph  
`{`: jump to previous paragraph  
`5gg` or `5G`: jump to line 5  
`G`: jump to last line in the file  
`gg`: jump to first line in the file  
`CTRL+o`: jump back in previous cursor positions  
`CTRL+i`: jump forward in previous cursor positions  
`CTRL+t`: jump to the file/code you were editing before the last tag jump  

**Moving Screen**
`zz`: center screen on cursor  
`CTRL+y`: scroll up without moving cursor  
`CTRL+e`: scroll down without moving cursor  

**Insert**
`i`: insert before the cursor  
`a`: insert after the cursor  
`I`: insert at the beginning of the line  
`A`: insert at the end of the line  
`o`: open a new line below the current line  
`O`: open a new line above the current line  
`s`: delete current character and enter edit

`C`: delete rest of line and enter edit  
`cc` or `S`: delete line and enter edit  

**In Insert Mode**
`CTRL+w`: delete word before cursor
`CTRL+u`: delete line before cursor
`CTRL+r {register}`: insert register content

`v`: enter visual (select) mode  
ESC or `CTRL+C`: exits visual mode  
`V`: enter visual mode and select line  

(in visual mode normal movement can be used to modify selection)

**In visual (select) mode**  
*Moving cursor commands apply.*  
	`i` inside   or   `a` around  
		`s`: current sentence  
		`p`: current paragraph  
		`"`: "..."  
		`'`: '...'  
		`(` or `b`: (...)  
		`{` or `B`: {...}  
		`[`: [...]  
		`<`: <...>  
	`d`: delete selection  
	`c`: delete selection and insert mode  

`o`: move to other end of selected text  

`r`: replace single character  
`~`: change character case

`dd`: delete current line  
`2dd`: delete 2 lines etc  
`D`: delete to end of line  
`x`: delete current character  
`X`: delete previous character

`d`: delete   or   `c`: delete and edit  
*then same selection motions as visual mode `i` and `a`, no cursor movement*  

`yy` or `Y`: yank line (note: `p` or `P` following `yy` pastes the line after or before the current line no matter where the cursor is)  
`2yy`: yank 2 lines etc  

`y`: yank (copy) selection  
*then same selection motions as visual mode `i` and `a`, no cursor movement*  

`"*y`: yank selection to system clipboard  
`"0y`: yank selection to register 0  
`"0p`: paste register 0  

`p`: paste yanked after cursor  
`P`: paste yanked before cursor  

`.`: repeat last action  

`J`: merge current line with line below with a space in-between  
`gJ`: merge current line with line below  

`u`: undo last change  
`CTRL+r`: redo change  

`gd`: jump to definition (example function name to declaration)  

`[(`: jump to previous opening of (...)
`])`: jump to closing of current (...)
etc with {...} [...] <...>

`*`: search for current word  
`/`: start search forward, press ENTER to jump to occurrence  
`?`: start search backwards  
`n`: next search result  
`N`: previous search result  
in "/" `CTRL+r 0`: paste register value 0 in search

`ma`: bookmarks cursor position as 'a'  
\`a: jump to bookmark a at same column
`'a`: jump to bookmark 'a'  start of line
\`\` or `''`: jump between last positions  
\`. or '.: jump to where the last editing was done  

`ZQ` or `:q`: close without saving  
`ZZ`: save and close  

`:%s/from/to/g`: replaces all "from" with "to" in file  
`:%s/from/to/gc`: replaces all "from" with "to" in file with confirmation  
`:s/from/to`: replaces all "from" with "to" in selection or line; use `n` and `.` to find next and repeat  

`cgn`: delete and edit selection then `ESC` then `n`, `.` to replace next occurrence with same command etc

`:reg`: display registers

todo: registers, marks, macro, search regexp grouping swapping

`CTRL+v`: enter visual mode in vertical mode where several lines can be edited  
`SHIFT+i` or `SHIFT+a`: multi-line edit

**Macros**  
`qa`: start recording macro a  
`q`: finish recording macro  
`@a`: run macro a