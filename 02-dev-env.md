# 開発環境

## C/C++

```shell
$ sudo apt install build-essential cmake
$ g++ --version
g++ (Debian 10.2.1-6) 10.2.1 20210110
Copyright (C) 2020 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
$ cmake --version
cmake version 3.18.4

CMake suite maintained and supported by Kitware (kitware.com/cmake).
```

## Python

Python 3.9.2 とかなり新しいバージョンがインストールされている。

```shell
$ python3 --version
Python 3.9.2
```

pipをインストール

```shell
$ sudo apt install python3-pip
$ pip --version
pip 20.3.4 from /usr/lib/python3/dist-packages/pip (python 3.9)
```

numpy, scipy, matplotlib, ipython, pandas等をインストールする。

```shell
pip install numpy scipy matplotlib ipython pandas
```

ほかは必要な時にインストールすることにする。

## golang

公式リポジトリにあるgoのバージョンを確認。

```shell
$ apt info golang
Package: golang
Version: 2:1.15~1
Priority: optional
Section: golang
Source: golang-defaults
Maintainer: Go Compiler Team <team+go-compiler@tracker.debian.org>
Installed-Size: 11.3 kB
Depends: golang-1.15, golang-doc (>= 2:1.15~1), golang-go (>= 2:1.15~1), golang-src (>= 2:1.15~1)
Homepage: https://golang.org
Download-Size: 4,844 B
APT-Sources: https://deb.debian.org/debian bullseye/main arm64 Packages
Description: Go programming language compiler - metapackage
 The Go programming language is an open source project to make
 programmers more productive. Go is expressive, concise, clean, and
 efficient. Its concurrency mechanisms make it easy to write programs
 that get the most out of multicore and networked machines, while its
 novel type system enables flexible and modular program construction.
 Go compiles quickly to machine code yet has the convenience of
 garbage collection and the power of run-time reflection. It's a
 fast, statically typed, compiled language that feels like a
 dynamically typed, interpreted language.
 .
 This package is a metapackage that, when installed, guarantees
 that (most of) a full Go development environment is installed.
```

`1.15`とちょっと古いが、とりあえずそれをインストールする。

```shell
$ sudo apt install golang
$ go version
go version go1.15.9 linux/arm64
```

gitリポジトリ管理ツールをインストールする。

```shell
go get github.com/x-motemen/ghq
```

実行ファイルは`~/go/bin/`にインストールされるので、PATHに追加する

```bash
PATH=$PATH:~/go/bin
```

PATH追加後に、ghqのバージョンを確認

```shell
$ vi ~/.bashrc 
$ source ~/.bashrc 
$ ghq --version
ghq version 1.2.1 (rev:HEAD)
```

ついでに、一緒に使用する`peco`をインストールする。

```shell
sudo apt install peco
```

## Rust

[公式の方法](https://www.rust-lang.org/tools/install)でインストールする。

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

インストールが終わったら、`~/.cargo/bin`をPATHに追加

```shell
$ rustc --version
rustc 1.57.0 (f1edd0429 2021-11-29)
```

よく使うrust製ツールをインストール。

```shell
cargo install lsd
cargo install bat
```

## git関連ツール

### tig

コンソール上に使うgitブラウザ

```shell
sudo apt install tig
```

### gitk

たまにGUIでブランチを確認時に使う

```shell
sudo apt install gitk
```

### git-delta

コンソールで差分表示を少しきれいにするツール

rust製、`cargo`でインストール

```shell
cargo install git-delta
```

インストールが終わったら、`~/.gitconfig`に以下を追加

```gitconfig
[core]
    pager = delta

[delta]
    line-numbers = true
    side-by-side = true
```
