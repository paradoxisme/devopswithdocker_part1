FROM ubuntu:20.04
WORKDIR /app

RUN apt update && apt install -y curl && \
    curl -sL https://deb.nodesource.com/setup_14.x | bash && \
    apt update && apt install -y nodejs && node -v && npm -v && \
    rm -rf /var/lib/apt/lists/* && \
    npm install

ENTRYPOINT npm run build && npm install -g serve && serve -s -l 5000 build

