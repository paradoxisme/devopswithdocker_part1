# Need
You need to clone https://github.com/docker-hy/material-applications.git projects

# For building:
```docker build -t node .```

# For running the container : 
```docker run --rm -p 5000:5000 -v "$PWD/material-applications/example-frontend":/app -it node```
