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
```
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
```
$ pip install numpy scipy matplotlib ipython pandas
```
ほかは必要な時にインストールすることにする。
