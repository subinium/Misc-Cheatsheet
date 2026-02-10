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
- Requires a [Nerd Font](https://www.nerdfonts.com/) for icons (e.g. `brew install --cask font-fira-code-nerd-font`)

``` sh
brew install eza
eza -la --icons --git
```

Recommended aliases:

```sh
alias ls='eza --icons'
alias ll='eza -la --icons --git'
alias lt='eza --tree --level=2 --icons'
```

## Modern find replacement (`fd`)

- https://github.com/sharkdp/fd
- Simple, fast, and user-friendly alternative to `find`
- Respects `.gitignore` by default

``` sh
brew install fd
fd "\.json$"          # find all .json files
fd -e py              # find all .py files
fd -H config          # include hidden files
```

## Smarter cd (`zoxide`)

- https://github.com/ajeetdsouza/zoxide
- Learns your most visited directories and lets you jump with `z`
- Replaces `cd`, `autojump`, `fasd`, `z.sh`

``` sh
brew install zoxide
eval "$(zoxide init zsh)"    # add to .zshrc
z projects                   # jump to most visited dir matching "projects"
zi                           # interactive selection with fzf
```

## Better git diff (`delta`)

- https://github.com/dandavison/delta
- Syntax highlighting, line numbers, side-by-side view for git diffs

``` sh
brew install git-delta
```

Add to `~/.gitconfig`:

```ini
[core]
    pager = delta
[interactive]
    diffFilter = delta --color-only
[delta]
    navigate = true
    side-by-side = true
[merge]
    conflictstyle = zdiff3
```

## Shell history search (`atuin`)

- https://github.com/atuinsh/atuin
- Replaces Ctrl+R with a full-featured history search (SQLite-backed)
- Supports fuzzy search, filtering by directory/session, and cross-device sync

``` sh
brew install atuin
eval "$(atuin init zsh)"     # add to .zshrc
```

## Terminal git UI (`lazygit`)

- https://github.com/jesseduffield/lazygit
- Full-featured git TUI: staging, branching, rebasing, stashing all in one view

``` sh
brew install lazygit
lazygit
```

## System monitor (`btop`)

- https://github.com/aristocratos/btop
- Beautiful TUI for CPU, memory, disk, network, and process monitoring
- Replaces `top`, `htop`

``` sh
brew install btop
btop
```

## Disk usage visualizer (`dust`)

- https://github.com/bootandy/dust
- Intuitive alternative to `du` with a visual bar chart

``` sh
brew install dust
dust            # current directory
dust /home      # specific path
```
