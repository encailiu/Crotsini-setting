# テキストエディタ

## neovim

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

## VSCode

[公式ページ](https://code.visualstudio.com/download#)から、ARM 64のdebファイルをダウンロードしてインストール。

```shell
sudo apt install ./code_1.62.3-1637136385_arm64.deb
```
