```
sudo dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo

sudo dnf -y install docker-ce docker-ce-cli containerd.io docker-compose-plugin

sudo systemctl --now enable docker

sudo usermod -a -G docker $(whoami)

```