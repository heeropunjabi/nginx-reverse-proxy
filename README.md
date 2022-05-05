# nginx-reverse-proxy

### Build reverse proxy image.
    docker build -t reverse-proxy .

### Run Nginx Reverse proxy server
    docker run -d --name reverse-proxy -p 8080:80 reverse-proxy    

### stop the container and remove the container.
    docker ps -q --filter ancestor="reverse-proxy" | xargs -r docker stop && docker rm -v $(docker ps -a -q -f status=exited)
      