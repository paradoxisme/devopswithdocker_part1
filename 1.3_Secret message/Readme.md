 dam@dam:~$ docker run -d -it devopsdockeruh/simple-web-service:ubuntu
4fb2a1d7e1a2592753fa440ffa93d262947d08beebd419a3316d0a254c4f9486
dam@dam:~$ docker ps
CONTAINER ID   IMAGE                                      COMMAND                 CREATED         STATUS         PORTS     NAMES
4fb2a1d7e1a2   devopsdockeruh/simple-web-service:ubuntu   "/usr/src/app/server"   3 seconds ago   Up 2 seconds             gifted_nash
dam@dam:~$ docker exec -it 4fb2a1d7e1a2 bash
root@4fb2a1d7e1a2:/usr/src/app# tail -f text.log 
2021-06-23 20:01:14 +0000 UTC
2021-06-23 20:01:16 +0000 UTC
2021-06-23 20:01:18 +0000 UTC
2021-06-23 20:01:20 +0000 UTC
2021-06-23 20:01:22 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-06-23 20:01:24 +0000 UTC
2021-06-23 20:01:26 +0000 UTC
2021-06-23 20:01:28 +0000 UTC
2021-06-23 20:01:30 +0000 UTC
2021-06-23 20:01:32 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
