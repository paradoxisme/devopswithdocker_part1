# Need
You need to clone https://github.com/docker-hy/material-applications.git projects

# For building container:
docker build -f Dockerfile_back -t go .
docker build -f Dockerfile_front -t node .

# For building project
docker run --rm -v "$PWD/material-applications/example-backend":/app -it go go build

# For running the container : 
docker run --rm -p 8000:8000 -v "$PWD/material-applications/example-backend":/app -it go ./server
docker run --rm -p 5000:5000 -v "$PWD/material-applications/example-frontend":/app -it node

# use

Open firefox to http://localhost:5000 
