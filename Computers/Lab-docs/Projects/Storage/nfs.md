```shell
sudo dnf install nfs-utils
```
```shell
$ sudo systemctl enable --now nfs-server
```
```shell
$ sudo systemctl enable --now rpcbind
```
```shell
$ sudo mkdir -p /nfs/exports/myshare
```
```shell
$ echo "/nfs/exports/myshare 192.168.122.0/24(rw)" > /etc/exports
```
```shell
$ sudo chown root:staff /nfs/exports/myshare
$ sudo chmod 775 /nfs/exports/myshare
```
