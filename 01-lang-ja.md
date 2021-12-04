# 日本語設定

以下のページを参考にした。

[初期設定＆日本語入力を使えるようにする方法｜ChromebookでLinux](https://catalyst-wakaba.com/linux-on-chrome-os/)

## よく使うutilsをインストール

```shell
sudo apt install apt-utils
```

## 地域設定

インストール直後に `Asia/Tokyo` になっていたので、そのまま。

## localeとフォント設定

```shell
sudo apt install task-japanese locales-all fonts-ipafont -y
sudo localectl set-locale LANG=ja_JP.UTF-8 LANGUAGE="ja_JP:ja"
source /etc/default/locale
```

設定後に、ターミナルで日本語が表示できるようになる。

```shell
$ ls -al
合計 28
drwxr-xr-x 1 ryu-o ryu-o  180 12月  3 22:58 .
drwxr-xr-x 1 root  root    10 12月  3 22:48 ..
-rw------- 1 ryu-o ryu-o  104 12月  3 22:49 .Xauthority
-rw------- 1 ryu-o ryu-o   30 12月  3 22:58 .bash_history
-rw-r--r-- 1 ryu-o ryu-o  220 12月  3 22:48 .bash_logout
-rw-r--r-- 1 ryu-o ryu-o 3526 12月  3 22:48 .bashrc
drwxr-xr-x 1 ryu-o ryu-o   20 12月  3 22:51 .cache
drwxr-xr-x 1 ryu-o ryu-o   62 12月  3 22:49 .config
drwx------ 1 ryu-o ryu-o   10 12月  3 22:51 .local
-rw-r--r-- 1 ryu-o ryu-o  807 12月  3 22:48 .profile
-rw-r--r-- 1 ryu-o ryu-o  448 12月  3 22:48 .sommelierrc
-rw------- 1 ryu-o ryu-o  756 12月  3 22:53 .viminf
```

## 日本語入力方法インストール

```shell
sudo apt install fcitx-mozc -y
```

## 環境変数の設定

```shell
sudo -e /etc/systemd/user/cros-garcon.service.d/cros-garcon-override.conf
```

で環境変数設定ファイルを開いて、後ろに以下の4行を追加する。

```conf
Environment="GTK_IM_MODULE=fcitx"
Environment="QT_IM_MODULE=fcitx"
Environment="XMODIFIERS=@im=fcitx"
Environment="GDK_BACKEND=x11"
```

他に、参考ページにあった`自動起動の設定`と`Mozcを追加`の作業をしなくても普通に使えているので、やっていない。

## Mozcの設定

```shell
/usr/lib/mozc/mozc_tool --mode=config_dialog
```

スペースは常に半角に設定する。
