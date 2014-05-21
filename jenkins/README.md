
Pull docker image:
```
docker pull baijum/jenkins
```

Example run:

```
docker.io run -d -p 9876:9876 -p 9877:9877 -v /var/lib/jenkins:/var/lib/jenkins baijum/jenkins 
```
