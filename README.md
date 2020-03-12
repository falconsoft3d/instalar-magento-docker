# Instalar Magento Docker

# 1 - Actualizamos el Sistema
```
sudo su
apt-get update && apt-get upgrade -y
apt  install docker.io
```

# 2 - Instalamos Portainer
```
docker pull portainer/portainer
docker run -d -p 9000:9000 -p 8000:8000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v /path/on/host/data:/data portainer/portainer
```

# 3 - Clonamos el repo de Magento
```
https://github.com/falconsoft3d/docker-magento
```

# 4 - Instalamos Magento
```
apt-get install docker-compose
docker-compose up -d
```






