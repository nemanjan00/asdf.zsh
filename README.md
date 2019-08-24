# asdf.zsh

a zsh plugin for auto-switching node versions based on project environment using [asdf](https://asdf-vm.com/)

## installation

### prerequisites

- jq

```bash
brew install jq
```

### antigen

```bash
antigen bundle nemanjan00/asdf.zsh
```

### zplugin

```bash
zplugin load nemanjan00/asdf.zsh
```

### zgen

```bash
zgen load nemanjan00/asdf.zsh
```

### oh-my-zsh

- cd `~/.oh-my-zsh/custom/plugins`
- `git clone https://github.com/nemanjan00/asdf.zsh`
- add `asdf.zsh` to `plugins=()` in your `.zshrc`

## usage

on its own, `asdf.zsh` will check for a `package.json` in the current directory. if it exists, it checks and reads the value of the node engine, and then switches to that version using n.

if the node engine reads 'greater than', `n` switches to node stable. otherwise, it switches to the specified version.
