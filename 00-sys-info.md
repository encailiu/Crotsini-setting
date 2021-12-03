# システム情報を確認

## マシン情報

[Lenovo Ideapad Duet](https://www.lenovo.com/jp/ja/notebooks/ideapad/duet-3-series/Lenovo-CT-X636/p/ZZICZCTCT1X)

- MediaTek Helio P60T プロセッサー (2GHz)
- 10.1" WUXGA IPS LEDバックライト 光沢あり マルチタッチ対応(10点) 1920x1200
- 4 GB LPDDR4X (オンボード)
- 128 GB SSD

## ChromeOSのバージョン

バージョン: 94.0.4606.124（Official Build） （32 ビット）

`chrome://flags/`のページで`Debian version for new Crostini containers`を`Bullseye`に設定すると、Debian 11が使えるようになる。

## Linuxのバージョン

```shell
$ hostnamectl
   Static hostname: penguin
         Icon name: computer-container
           Chassis: container
        Machine ID: d5c2758f8e23335df490a876612dab20
           Boot ID: 827f8883f145422c957e36c67893bcb7
    Virtualization: lxc
  Operating System: Debian GNU/Linux 11 (bullseye)
            Kernel: Linux 5.4.139-16311-g330b3df0010b
      Architecture: arm64
$ cat /etc/os-release 
PRETTY_NAME="Debian GNU/Linux 11 (bullseye)"
NAME="Debian GNU/Linux"
VERSION_ID="11"
VERSION="11 (bullseye)"
VERSION_CODENAME=bullseye
ID=debian
HOME_URL="https://www.debian.org/"
SUPPORT_URL="https://www.debian.org/support"
BUG_REPORT_URL="https://bugs.debian.org/"
```

## システム更新後の使用ディスク容量

```shell
$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/vdc         32G  1.9G   30G   6% /
none            492K     0  492K   0% /dev
devtmpfs        1.4G     0  1.4G   0% /dev/tty
/dev/vdc         32G  1.9G   30G   6% /dev/wl0
tmpfs           100K     0  100K   0% /dev/lxd
tmpfs           100K     0  100K   0% /dev/.lxd-mounts
run             1.4G   28K  1.4G   1% /dev/.host_ip
/dev/root       235M  231M     0 100% /dev/.ssh/sshd_config
9p              2.0G  740K  2.0G   1% /mnt/chromeos
tmpfs           1.4G     0  1.4G   0% /mnt/external
/dev/vdb         35M   35M     0 100% /opt/google/cros-containers
tmpfs           1.4G     0  1.4G   0% /dev/shm
tmpfs           557M  124K  557M   1% /run
tmpfs           5.0M     0  5.0M   0% /run/lock
tmpfs           4.0M     0  4.0M   0% /sys/fs/cgroup
tmpfs           279M   32K  279M   1% /run/user/1000
```
