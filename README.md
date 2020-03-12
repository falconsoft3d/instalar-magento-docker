# Paso a paso para instalar Magento ver. 1.9.3.8 con Docker en Ubuntu 18.04

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
git clone https://github.com/falconsoft3d/docker-magento
cd docker-magento
```

# 4 - Instalamos Magento
```
apt-get install docker-compose
docker-compose up -d
```

# 5- Nos conectamos a Portainer para sacar el ip
```
host: 172.18.0.2
user: root
pass: myrootpassword
```

# Constraseñas
```
MYSQL_HOST=db
MYSQL_ROOT_PASSWORD=myrootpassword
MYSQL_USER=magento
MYSQL_PASSWORD=magento
MYSQL_DATABASE=magento

MAGENTO_LOCALE=en_GB
MAGENTO_TIMEZONE=Pacific/Auckland
MAGENTO_DEFAULT_CURRENCY=NZD
MAGENTO_URL=http://local.magento

MAGENTO_ADMIN_FIRSTNAME=Admin
MAGENTO_ADMIN_LASTNAME=MyStore
MAGENTO_ADMIN_EMAIL=amdin@example.com
MAGENTO_ADMIN_USERNAME=admin
MAGENTO_ADMIN_PASSWORD=magentorocks1
```






