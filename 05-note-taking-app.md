# メモ用アプリ

[flatpak](https://flatpak.org/setup/Chrome%20OS/)から[Obsidian](https://obsidian.md/)をインストールする。

## flatpakセットアップ

### flatpakをインストール

```shell
sudo apt install flatpak
```

### falthub のリポジトリを追加

```shell
flatpak --user remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

### リブートLinux

```shell
sudo reboot
```

実行するとターミナルが自動的に落ちるので、もう一回立ち上げる。

## Obsidian をインストール

[Obisidian-Linux App on Flathub](https://flathub.org/apps/details/md.obsidian.Obsidian)に書かれた通りにインストールすれば良い。

```shell
flatpak install flathub md.obsidian.Obsidian
```

実行するには、

```shell
flatpak run md.obsidian.Obsidian
```

実行すると、

```shell
$ flatpak run md.obsidian.Obsidian
bwrap: Can't mount proc on /newroot/proc: Operation not permitted
error: ldconfig failed, exit status 256
```

と怒られた。

https://www.reddit.com/r/Crostini/comments/qj610m/flatpak_broken_on_version_960466425_official/
によると、Debian 11コンテナだけの問題らしい。Debian 10にしたら治るみたいだけど、しばらく待ってみるか？
