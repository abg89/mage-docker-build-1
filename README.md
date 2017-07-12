# Magento docker builder

### Install docker and docker-compose

```
curl -L https://get.docker.com/ | sh
sudo usermod -aG docker $(whoami)
sudo systemctl enable --now docker.service
curl -L --fail https://github.com/docker/compose/releases/download/1.14.0/run.sh > /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

### Get and run docker environment

```
git clone https://github.com/g4xd/mage-docker-build.git
cd mage-build
docker-compose up -d --build
```

### Install magento
```
docker-compose exec mage magento-install
```
