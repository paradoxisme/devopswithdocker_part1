```
dam@dam:~$ docker images
REPOSITORY                          TAG       IMAGE ID       CREATED        SIZE
ubuntu                              latest    9873176a8ff5   8 days ago     72.7MB
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   3 months ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   3 months ago   15.7MB
```
 
```
dam@dam:~$ docker pull devopsdockeruh/simple-web-service:ubuntu
ubuntu: Pulling from devopsdockeruh/simple-web-service
Digest: sha256:d44e1dce398732e18c7c2bad9416a072f719af33498302b02929d4c112e88d2a
Status: Image is up to date for devopsdockeruh/simple-web-service:ubuntu
docker.io/devopsdockeruh/simple-web-service:ubuntu
```

```
dam@dam:~$ docker pull devopsdockeruh/simple-web-service:alpine
alpine: Pulling from devopsdockeruh/simple-web-service
ba3557a56b15: Pull complete 
1dace236434b: Pull complete 
4f4fb700ef54: Pull complete 
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Downloaded newer image for devopsdockeruh/simple-web-service:alpine
docker.io/devopsdockeruh/simple-web-service:alpine
```

```
dam@dam:~$ docker images
REPOSITORY                          TAG       IMAGE ID       CREATED        SIZE
ubuntu                              latest    9873176a8ff5   8 days ago     72.7MB
devopsdockeruh/simple-web-service   ubuntu    4e3362e907d5   3 months ago   83MB
devopsdockeruh/simple-web-service   alpine    fd312adc88e0   3 months ago   15.7MB
```

```
dam@dam:~$ docker run -d -it devopsdockeruh/simple-web-service:alpine
9775155e86a88be5995d90fd87e5c199fa3dad0cc699aa45133670d78a444ecc
```

```
dam@dam:~$ docker exec -it 9775155e86a8 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
Input website:
helsinki.fi
Searching..
sh: curl: not found
```

```
dam@dam:~$ docker exec -it 9775155e86a8 sh
/usr/src/app # apk add curl
fetch https://dl-cdn.alpinelinux.org/alpine/v3.13/main/x86_64/APKINDEX.tar.gz
fetch https://dl-cdn.alpinelinux.org/alpine/v3.13/community/x86_64/APKINDEX.tar.gz
(1/5) Installing ca-certificates (20191127-r5)
(2/5) Installing brotli-libs (1.0.9-r3)
(3/5) Installing nghttp2-libs (1.42.0-r1)
(4/5) Installing libcurl (7.77.0-r1)
(5/5) Installing curl (7.77.0-r1)
Executing busybox-1.32.1-r3.trigger
Executing ca-certificates-20191127-r5.trigger
OK: 8 MiB in 19 packages
/usr/src/app # 
```

```
dam@dam:~$ docker exec -it 9775155e86a8 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
```
