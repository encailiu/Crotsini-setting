# テキストエディタ

## vim

### プラグインマネージャ

[Vundle](https://github.com/VundleVim/Vundle.vim)を使用。

プラグインマネージャを取得：

```shell
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

`.vimrc`でVundleを設定

```vimrc
""" プラグインマネージャーVundle                                                                                                                   
set nocompatible
filetype off 
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'VundleVim/Vundle.vim'

" 導入したいプラグインを以下に列挙
" Plugin '[Github Author]/[Github repo]' の形式で記入
Plugin 'ervandew/supertab'       " tabで補完

call vundle#end()
"filetype plugin indent on
filetype plugin on

" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ

""" その他カスタマイズ設定は以下に記載す
```

### ファイラー

VIMプラグイン[Fern](https://github.com/lambdalisue/fern.vim)を使う

`.vimrc`の『導入したいプラグイン』に`Plugin 'lambdalisue/fern.vim'`を追加して`:PluginInstall`でインストールする。

```vimrc
" 導入したいプラグインを以下に列挙
" Plugin '[Github Author]/[Github repo]' の形式で記入
Plugin 'ervandew/supertab'       " tabで補完
Plugin 'lambdalisue/fern.vim'    " tree viewer
```

### ブロックコメント

[NERD Commenter](https://github.com/preservim/nerdcommenter)を使う。

『導入したいプラグイン』の所に`Plugin 'preservim/nerdcommenter'`を追加して、`:PluginInstall`でインストールする。

```vimrc
" 導入したいプラグインを以下に列挙
" Plugin '[Github Author]/[Github repo]' の形式で記入
Plugin 'ervandew/supertab'       " tabで補完
Plugin 'lambdalisue/fern.vim'    " tree viewer
Plugin 'preservim/nerdcommenter' " blockコメント
```

## neovim

**インストールしたが、とりあえずVIMで困っていないので、しばらくVIMを使うようにする。**

```shell
$ sudo apt install neovim
$ nvim --version
NVIM v0.4.4
Build type: Release
Lua 5.1
Compilation: /usr/bin/cc -g -O2 -fdebug-prefix-map=/build/neovim-AMNr6D/neovim-0.4.4=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=1 -DDISABLE_LOG -Wdate-time -D_FORTIFY_SOURCE=1 -O2 -DNDEBUG -DMIN_LOG_LEVEL=3 -Wall -Wextra -pedantic -Wno-unused-parameter -Wstrict-prototypes -std=gnu99 -Wshadow -Wconversion -Wmissing-prototypes -Wimplicit-fallthrough -Wvla -fstack-protector-strong -fno-common -fdiagnostics-color=always -DINCLUDE_GENERATED_DECLARATIONS -D_GNU_SOURCE -DNVIM_MSGPACK_HAS_FLOAT32 -DNVIM_UNIBI_HAS_VAR_FROM -I/build/neovim-AMNr6D/neovim-0.4.4/build/config -I/build/neovim-AMNr6D/neovim-0.4.4/src -I/usr/include -I/usr/include/lua5.1 -I/build/neovim-AMNr6D/neovim-0.4.4/build/src/nvim/auto -I/build/neovim-AMNr6D/neovim-0.4.4/build/include
Compiled by team+vim@tracker.debian.org

Features: +acl +iconv +tui
See ":help feature-compile"

   system vimrc file: "$VIM/sysinit.vim"
  fall-back for $VIM: "/usr/share/nvim"

Run :checkhealth for more info
```

## ~~VSCode~~

**[vsvode.dev](https://vscode.dev/)でものがたりでいるので、ローカルにインストールしているものを削除した**

~~[公式ページ](https://code.visualstudio.com/download#)から、ARM 64のdebファイルをダウンロードしてインストール。~~

```shell
sudo apt install ./code_1.62.3-1637136385_arm64.deb
```
