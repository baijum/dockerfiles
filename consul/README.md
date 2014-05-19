
Pull docker image:
```
docker pull baijum/consul
```

Example run:

```
docker.io run -d -p 8500:8500 -v /var/consul:/var/consul baijum/consul -server -bootstrap -client=0.0.0.0 -data-dir /var/consul -ui-dir /usr/local/share/consul
```
