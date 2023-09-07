# zsh eza plugin

Small zsh plugin to add useful aliases for [eza](https://github.com/eza-community/eza).

## What it does

```bash
# Group directories first, show icons, and enable file size color scale
alias ls='eza --group-directories-first --icons --color-scale'
alias lt='eza --tree --level=2 --icons' # Show in tree view
alias l='ls -a'                         # Short, all files
alias ld='l -D'                         # Short, only directories
alias ll='ls -lbG --git'                # Long, file size prefixes, grid, git status
alias la='ll -a'                        # Long, all files
alias lC='la --sort=changed'            # Long, sort changed
alias lM='la --sort=modified'           # Long, sort modified
alias lS='la --sort=size'               # Long, sort size
alias lX='la --sort=extension'          # Long, sort extension
```

## What it needs

- zsh
- eza
- patched font with glyphs

## Get it

Install eza, for platform specific [installation instructions check here](https://github.com/eza-community/eza#installation).

You will also need a patched font with icons (glyphs).  
I recommend using one of the [nerd-fonts](https://github.com/ryanoasis/nerd-fonts).

### Oh My Zsh

Clone zsh-eza to your `$ZSH_CUSTOM` plugins directory.

```bash
git clone https://github.com/JPDVM2014/zsh-eza.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-eza
```

Then add zsh-eza to your plugins array in your `.zshrc` file.

```bash
plugins=(.. zsh-eza)
```

### Manual install

Clone zsh-eza and add `source <zsh-eza-dir>/zsh-eza.plugin.zsh` to your `.zshrc` file.

```bash
git clone https://github.com/JPDVM2014/zsh-eza.git
echo "source `pwd`/zsh-eza/zsh-eza.plugin.zsh" >> ~/.zshrc
```
