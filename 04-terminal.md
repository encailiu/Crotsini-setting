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
```bashrc
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
