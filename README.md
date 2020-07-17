Email sender service, using reverse proxy with nginx, python app, python scalable workers, queue with redis and postgres as persistent database.

Useful commands:
docker-compose ps       ## list running containers
docker-compose up -d         ## start containers from compose
docker-compose down         ## stop running containers
docker-compose logs -f -t       ## show logs from containers
docker-compose up -d --scale worker=3       ## start containers with scalability
docker-compose exec db psql -U postgres -d email_sender -c "select * from emails"       # run a db query