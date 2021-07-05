dam@dam:~/Bureau$ docker run --rm -p 8080:8080 -it devopsdockeruh/simple-web-service server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
[GIN] 2021/06/27 - 13:28:07 | 200 |      49.443µs |      172.17.0.1 | GET      "/"

[GIN] 2021/06/27 - 13:29:54 | 200 |      57.879µs |      172.17.0.1 | GET      "/"


Open firefox with this address : 127.0.0.1:8080

or with curl:

dam@dam:~/Bureau$ curl 127.0.0.1:8080
{"message":"You connected to the following path: /","path":"/"}
