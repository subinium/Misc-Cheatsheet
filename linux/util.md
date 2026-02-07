## Prevent laptop from sleeping (`caffeinate`)

- Keeps your machine awake during local tasks like data preprocessing
- For remote servers, use `tmux` instead

``` sh
caffeinate
```

## Count files in a directory (`ls -l | grep ^- | wc -l`)

``` sh
ls -l | grep ^- | wc -l
```

## Check remaining disk space (`df -h`)

- Shows disk usage across the entire Linux system
- The `-h` option displays sizes in MB/GB for readability

``` sh
df -h
```

## Use cat with syntax highlighting (`bat`)

- Similar to `cat` but with syntax highlighting

``` sh
brew install bat
bat <file>
```

Tip: alias it to `cat` for everyday use.

```
alias cat="bat"
```

## Keep directory when opening new tab in iTerm

- Go to iTerm Preferences > Profiles > Working Directory > Advanced Configuration > Edit
- Set "Working Directory for New Tabs" to "Reuse previous session's directory"

## Create shortcuts with symbolic links (`ln -s`)

- Creates a shortcut (symlink) to a target path

``` sh
ln -s [target path] [source path]
```

## Suppress pip install output (`pip install` with `-q`, `-qq`, `-qqq`)

- When installing packages via pip in Jupyter Notebook, output can clutter the view
- Same applies to the shell
- Use `-q`, `-qq`, or `-qqq` to suppress output:
  - `-q` : Show WARNING, ERROR, CRITICAL only
  - `-qq` : Show ERROR, CRITICAL only
  - `-qqq` : Show CRITICAL only

```
pip install -qqq <library>
```

## Enable mouse in tmux (`set -g mouse on`)

- To enable mouse in tmux, uncomment the following in `.tmux/.tmux.conf.local`

```
# start with mouse mode enabled
set -g mouse on
```

## Pretty-print JSON files (`jq`)

- Pretty-prints JSON

```
brew install jq
jq . test.json
```

## Font recommendation (`D2 Coding`)

- Recommended coding font
- [naver/d2codingfont](https://github.com/naver/d2codingfont)

## Simplified man pages (`tldr`)

- Community-driven man pages with practical examples
- Much easier to read than `man`

``` sh
brew install tldr
tldr tar
```

## Fuzzy finder for everything (`fzf`)

- https://github.com/junegunn/fzf
- Interactive fuzzy finder for files, command history, and more
- Integrates with Ctrl+R for history search, Ctrl+T for file search

``` sh
brew install fzf
```

## Modern ls replacement (`eza`)

- https://github.com/eza-community/eza
- A modern replacement for `ls` with colors, icons, and git integration

``` sh
brew install eza
eza -la --icons --git
```
