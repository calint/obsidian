`h,j,k,l`: move cursor
`CTRL+u/d`: move cursor half a screen up/down
`zz`: center screen on cursor
`M`: move cursor to middle of screen
`i`: insert before the cursor
`a`: insert (append) after the cursor
`I`: insert at the beginning of the line
`A`: insert (append) at the end of the line
`o`: append (open) a new line below the current line
`O`: append (open) a new line above the current line
`ea`: insert (append) at the end of the word
`^`: jump to first character of line
`0`: jump to start of line
`$`: jump to end of line
`w`: jump one word forward
`W`: jump one word including punctuation forward
`b`: jump one word backwards
`B`: jump one word including punctuation backwards
`e`: jump to end of word
`ge`: jump backwards to the end of a word
`gE`: jump backwards to the end of a word (words can contain punctuation)
`%`: jump to to matching character (default supported pairs: '()', '{}', '[]'
`}`: jump to next paragraph
`{`: jump to previous paragraph
`5gg` or `5G`: jump to line 5
`4k`: example jump up 4 lines. works with `h,j,k,l`

`CTRL+o`: jump back in previous cursor positions
`CTRL+i`: jump forward in previous cursor positions

`C`: delete rest of line and enter edit
`cc` or `S`: delete line and enter edit

`v`: enter visual (select) mode
ESC or `CTRL+C`: exist visual mode
`V`: enter visual (select) mode and select line

(in visual mode normal movement can be used to modify selection)

In visual (select) mode
	`i`  inside   or   `a` including delimiter
		`w`: current word
		`W`: current word including punctuation
		`s`: current sentence
		`p`: current paragraph
		`"`: "..."
		`(` or `b`: (...)
		`{` or `B`: {...}
		`[`: [...]
		`<`: <...>
	`d`: delete selection
	`c`: delete selection and insert mode

`o`: move to other end of selected text

`r`: replace single character

`dd`: delete current line
`d2d`: delete 2 lines etc
`D`: delete to end of line
`x`: delete current character

`d`: delete   or   `c`: delete and edit
	`w`: to end of current word
	`b`: to beginning of current word
	`$`: to end of line
	`i` inside   or   `a` including delimiter
		`w`: current word
		`W`: current word including punctuation
		`s`: current sentence
		`p`: current paragraph
		`"`: "..."
		`(` or `b`: (...)
		`{` or `B`: {...}
		`[`: [...]
		`<`: <...>
	
`J`: merge current line with line below with a space in-between
`gJ`: merge current line with line below

`yy`: yank line
`y2y`: yank 2 lines etc

`y`: yank (copy) selection
	`w`: word
	`$`: to end of line
	`i` for inside of   or   `a` including delimiter
		`w`: current word
		`W`: current word including punctuation
		`s`: current sentence
		`p`: current paragraph
		`"`: "..."
		`(` or `b`: (...)
		`{` or `B`: {...}
		`[`: [...]
		`<`: <...>

`p`: paste yanked after cursor
`P`: paste yanked before cursor

`u`: undo last change
`CTRL+r`: redo change

`gd`: jump to definition (example function name to declaration)

`fx`: jump to next occurrence of character x in line
`tx`: jump to before next occurrence of character x in line
`Fx`: jump to the previous occurrence of character x
`Tx`: jump to after previous occurrence of character x
`;` : repeat previous f, t, F or T movement
`,`: repeat previous f, t, F or T movement, backwards

`*`: search for current word
`/`: start search forward, press ENTER to jump to occurrence
`?`: start search backwards
`n`: next search result
`N`: previous search result

`ma`: bookmarks cursor position as 'a'
\`a or `'a`: jump to bookmark 'a'
\`\` or `''`: jump between last positions
\`. or '.: jump to where the last editing was done
`.`: repeat last action
`ZQ` or `:q`: close without saving
`ZZ`: save and close

todo: registers, marks, macro, search and replace
