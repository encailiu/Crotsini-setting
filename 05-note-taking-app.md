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
