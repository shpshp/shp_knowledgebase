Install Docker
==============

```bash
# Remove previous versions
sudo apt remove docker docker-engine docker.io

sudo apt install  curl  apt-transport-https ca-certificates software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update && sudo apt full-upgrade
sudo apt install docker-ce

# Check
sudo systemctl status docker
```

[Read more on the installation.](https://tecadmin.net/install-docker-on-ubuntu/)
