# Containerized Email Sender 
Email sender service, built to learn about Docker and Docker Compose.

# Installation and Setup
```shell
$ git clone https://github.com/victorpuntel/email-worker-compose.git
then
$ docker-compose up -d
```
The app can be acessed at `http://localhost`.
The api can be acessed at `http://localhost/api`. 

## Technologies
This service uses:
- Nginx to frontend page and reverse proxy
- Python to backend app
- Python to scalable workers
- Redis to queue
- Postgres to persistent database

## Useful commands:
`$ docker-compose ps`    ## list running containers
`$ docker-compose up -d`    ## start containers from compose
`$ docker-compose down`     ## stop running containers
`$ docker-compose logs -f -t`   ## show logs from containers
`$ docker-compose up -d --scale worker=3`   ## start containers with scalability
`$ docker-compose exec db psql -U postgres -d email_sender -c "select * from emails"`   # run a db query