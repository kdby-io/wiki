## MongoDB

# install

```bash
sudo apt-get update
sudo apt-get upgrade

# 이전버전 제거
sudo apt-get remove mongodb
sudo apt-get autoremove

sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.2.list
sudo apt-get update
apt-get install -y --allow-unauthenticated mongodb-org
```

# Failed to start mongodb.service: Unit mongodb.service not found.
/lib/systemd/system/mongodb.service 내용을 아래와 같이 넣어준다.
```
[Unit]
Description=High-performance, schema-free document-oriented database
After=network.target

[Service]
User=mongodb
ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf

[Install]
WantedBy=multi-user.target
```
