The best of: https://www.lazyvim.org/keymap

| General       |                            |              |
| ------------- | -------------------------- | ------------ |
| `gco`         | Add Comment Below          | **n**        |
| `gcO`         | Add Comment Above          | **n**        |
| `<leader>us`  | Toggle Spelling            | **n**        |
| `<leader>uA`  | Toggle Tabline             | **n**        |
| `<leader>uh`  | Toggle Inlay Hints         | **n**        |
| `<leader>\|`  | Split Window Right         | **n**        |
| `[b`          | Prev Buffer                | **n**        |
| `]b`          | Next Buffer                | **n**        |
| **Harpoon**   |                            |              |
| `<leader>1`   | Harpoon to File 1          | **n**        |
| `<leader>2`   | Harpoon to File 2          | **n**        |
| `<leader>3`   | Harpoon to File 3          | **n**        |
| `<leader>4`   | Harpoon to File 4          | **n**        |
| `<leader>5`   | Harpoon to File 5          | **n**        |
| `gco`         | Add Comment Below          | **n**        |
| `gcO`         | Add Comment Above          | **n**        |
| `<leader>us`  | Toggle Spelling            | **n**        |
| `<leader>uA`  | Toggle Tabline             | **n**        |
| `<leader>uh`  | Toggle Inlay Hints         | **n**        |
| `<leader>\|`  | Split Window Right         | **n**        |
| **LSP**       |                            |              |
| `<leader>cl`  | Lsp Info                   | **n**        |
| `gd`          | Goto Definition            | **n**        |
| `gr`          | References                 | **n**        |
| `gI`          | Goto Implementation        | **n**        |
| `gy`          | Goto T[y]pe Definition     | **n**        |
| `gD`          | Goto Declaration           | **n**        |
| `K`           | Hover                      | **n**        |
| `gK`          | Signature Help             | **n**        |
| `<c-k>`       | Signature Help             | **i**        |
| `<leader>ca`  | Code Action                | **n**, **v** |
| `<leader>cc`  | Run Codelens               | **n**, **v** |
| `<leader>cC`  | Refresh & Display Codelens | **n**        |
| `<leader>cR`  | Rename File                | **n**        |
| `<leader>cr`  | Rename                     | **n**        |
| `<leader>cA`  | Source Action              | **n**        |
| `]]`          | Next Reference             | **n**        |
| `[[`          | Prev Reference             | **n**        |
| `<a-n>`       | Next Reference             | **n**        |
| `<a-p>`       | Prev Reference             | **n**        |
| **Telescope** |                            |              |
| `<leader>ss`  | Goto Symbol (Aerial)       | **n**        |
| **Snacks**    |                            |              |
| `<leader>uC`  | Colorschemes               | **n**        |
|               |                            |              |

Useful commands: 
* `LazyExtras`
* `LspInfo`

 Tips:
 * after `K` for lsp pop-up press `K` again to enter pop-up window and scroll. exit with `q`
 * navigate autocomplete options with `C-n` and `C-p`
 * `]a` to jump to start of next function argument then `C+<space>` to select the argument followed by `c` to delete it and enter edit mode
 * `S+h` and `S+l` for previous and next buffer
 * `C+h,j,k,l` in split window jump to buffer left, down, up, right
 * `gr` shows references to symbol
 * `A+j,k` move selected lines down or up
 * `gc` comment out selected block
 * in explorer `i` to focus on search field
 * `cia` deletes function argument and enters edit mode, then `esc` and `cina` to repeat for next argument
 * `s` flash search
 * `<leader>sS` show types in workspace
* auto-completions move between object `C-n`/`C-p` select using `enter` or `tab`. jump to next argument using `tab`
* 