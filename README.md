docker ps
docker stop $(docker ps -aq) && docker rm $(docker ps -aq) && docker rmi  -f $(docker images -a -q)
docker compose -f docker-compose-no-build-frontend.yml up -d

docker compose up -d --build