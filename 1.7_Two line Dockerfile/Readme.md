```
dam@dam:~/Bureau/devopswithdocker/Two line Dockerfile$ docker build -t web-server .
Sending build context to Docker daemon  2.048kB
Step 1/2 : FROM devopsdockeruh/simple-web-service:alpine
 ---> fd312adc88e0
Step 2/2 : CMD server
 ---> Running in 51ae967e5757
Removing intermediate container 51ae967e5757
 ---> bdae1bb0a697
Successfully built bdae1bb0a697
Successfully tagged web-server:latest
```

```
dam@dam:~/Bureau/devopswithdocker/Two line Dockerfile$ docker run web-server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080
```
