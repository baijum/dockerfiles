
Pull docker image:
```
docker pull baijum/mongodb
```

Example run:

```
mkdir -p /var/mongodb/db
touch /var/mongodb/mongodb.conf
docker.io run -d -p 27017:27017 -p 28017:28017 -v /var/mongodb:/data baijum/mongodb -f /data/mongodb.conf
```
