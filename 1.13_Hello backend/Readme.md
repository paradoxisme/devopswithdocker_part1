# Need
You need to clone https://github.com/docker-hy/material-applications.git projects

# For building:
```
docker build -t go .
```

# For running the container : 
```
docker run --rm -v "$PWD/material-applications/example-backend":/app -it go go build
docker run --rm -p 8080:8080 -v "$PWD/material-applications/example-backend":/app -it go ./server
```
