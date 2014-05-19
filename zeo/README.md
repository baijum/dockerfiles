
Pull docker image:
```
docker pull baijum/zeo
```

Example run:

```
docker.io run -d -p 8600:8600 -p 8601:8601 -v /var/zeo:/var/zeo baijum/zeo -a 8600 -m 8601 -f /var/zeo/Data.fs
```
