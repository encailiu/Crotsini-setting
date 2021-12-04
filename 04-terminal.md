# Shellとターミナル関係

## [oh-my-bash](https://github.com/ohmybash/oh-my-bash)をインストール

```shell
bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmybash/oh-my-bash/master/tools/install.sh)"
```

[Oh-my-bash Themes](https://github.com/ohmybash/oh-my-bash/wiki/Themes)を参照してテーマだけ好きなものに変更：
```
$ vi ~/.bashrc
```
で設定ファイルを開いて、
```bash
# Set name of the theme to load. Optionally, if you set this to "random"
# it'll load a random theme each time that oh-my-bash is loaded.
# OSH_THEME="font"
OSH_THEME="brainy"
```

## ターミナル

Debian 10の時にあった、日本語入力時に表示位置がずれる問題が改善されていたので、そのまま標準のターミナルを使う。

## よく使用するツール

```shell
$ sudo apt install tree htop neofetch peco apt-utils
```
## よく使うalias、keybind設定等

```bash
# history
export HISTSIZE=10000
export HISTCONTROL=ignoreboth   # ignorespace+ignoredups = ignoreboth

peco-history() {
        local l=$(HISTTIMEFORMAT= history | \
        sort -r | sed -E s/^\ *[0-9]\+\ \+// | \
        peco --query "$READLINE_LINE")
        READLINE_LINE="$l"
        READLINE_POINT=${#l}
}
bind -x '"\C-r": peco-history'

# ls
alias ls="lsd"
alias la="lsd -a"
alias ll="lsd -al"

# git
function grl() {
  local selected_file=$(ghq list --full-path | peco --query "$LBUFFER")
  if [ -n "$selected_file" ]; then
    if [ -t 1 ]; then
      echo ${selected_file}
      cd ${selected_file}
    fi
  fi
}
bind -x '"\C-g": grl'

alias gpl="git pull"
alias pull="git pull"
alias gps="git push"
alias push="git push"
alias gst="git status"
alias gs="git status -s -b -u"
alias status="git status"
alias gco="git commit"
alias commit="git commit"
alias add="git add"
alias gd="git diff"

# PATH
PATH=$PATH:~/.local/bin:~/go/bin:~/.cargo/bin
. "$HOME/.cargo/env"

# cd
function peco-cd() {
  if [[ -z "$1" ]]; then
    local dir="$( find . -maxdepth 2 -type d | sed -e 's;\./;;' | peco )"
    if [ ! -z "$dir" ] ; then
      cd "$dir"
    fi
  else
    cd "$1"
  fi
}
alias pcd="peco-cd"
```