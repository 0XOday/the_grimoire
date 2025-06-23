```shell
sudo dnf install nfs-utils


$ sudo systemctl enable --now nfs-server


$ sudo systemctl enable --now rpcbind


$ sudo mkdir -p /nfs/exports/myshare


$ echo "/nfs/exports/myshare 192.168.122.0/24(rw)" > /etc/exports

$ sudo chown root:staff /nfs/exports/myshare

$ sudo chmod 775 /nfs/exports/myshare

$ sudo exportfs -r

$ sudo firewall-cmd --add-service nfs --permanent

$ 

```
