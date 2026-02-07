## (vimrc) File type detection and syntax highlighting (`syntax on`, `filetype indent plugin on`)

- Basic syntax highlighting without plugins

```
syntax on
filetype indent plugin on
```

## (vimrc) Highlight search, brackets, etc. (`hlsearch`, `ruler`, `showmatch`)

- `hlsearch` : Highlight search results
- `ruler` : Show current line info
- `showmatch` : Highlight matching brackets

```
set hlsearch
set ruler
set showmatch
```

## (vimrc) Convenient settings for Python editing (tab sizes, indentation)

- Adjust default tab size
- Auto indentation and indent settings

```
set tabstop=4
set softtabstop=4
set shiftwidth=4
set autoindent
```

## (vimrc) Show line numbers

- Display line numbers

```
set number  "line number
```

## (vimrc) Change cursor shape per mode

```
" cursor shape
let &t_SI = "\<Esc>]50;CursorShape=1\x7" " Vertical bar in insert mode
let &t_EI = "\<Esc>]50;CursorShape=0\x7" " Block in normal mode
let &t_SR = "\<esc>]50;CursorShape=2\x7" " Underline in replace mode
```

## Multi-line commenting in vim (`norm i#`, `norm 1x`)

- Select the desired lines in visual mode
- Use `norm` to insert `#` at the beginning of each line
- Replace `#` with the appropriate comment character for your language

```
:norm i#
```

- To remove comments, delete the first character of each line
- Replace `1` with another number to delete N characters

```
:norm 1x
```

## Save with sudo in vim (`w sudo! tee %`)

- Opened a file with vi but don't have write permission?
- Command breakdown:
  - `w` : write
  - `!sudo` : root privilege
  - `tee` : pass via stdin
  - `%` : current filename

```
:w sudo! tee %
```
