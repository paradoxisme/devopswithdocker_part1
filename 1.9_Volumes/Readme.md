```
dam@dam:~/Bureau$ mkdir share
dam@dam:~/Bureau$ docker run --rm -v $HOME/Bureau/share:/app -w /app -it devopsdockeruh/simple-web-service
Starting log output
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
Wrote text to /app/text.log
```

```
dam@dam:~/Bureau$ cat $HOME/Bureau/share/text.log 
2021-06-27 13:20:29 +0000 UTC
2021-06-27 13:20:31 +0000 UTC
2021-06-27 13:20:33 +0000 UTC
2021-06-27 13:20:35 +0000 UTC
2021-06-27 13:20:37 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-06-27 13:20:39 +0000 UTC
2021-06-27 13:20:41 +0000 UTC
2021-06-27 13:20:43 +0000 UTC
2021-06-27 13:20:45 +0000 UTC
2021-06-27 13:20:47 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-06-27 13:20:49 +0000 UTC 
```
