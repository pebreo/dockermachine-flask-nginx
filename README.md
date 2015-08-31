
Run docker-machine
-------------------
$ dma create -d virtualbox dev1;
$ deval dev1

Run docker-compose
-------------------
$ dc build 
$ dc up -d

Push to production
------------------
$ dma create \
-d digitalocean \
--digitalocean-access-token=ADD_YOUR_TOKEN_HERE \
--engine-opt log-driver=syslog \  
staging

dc build 
dc up -d 
docker-compose run web /usr/local/bin/python create_db.py


Other commands
dma ssh dev1
tail -f /var/log/syslog # on the host machine
dc ps
d exec -it <containerName> bash
psql -h 192.168.99.100 -p 5432 -U postgres --password


# Repo inspired by:
https://github.com/realpython/orchestrating-docker
