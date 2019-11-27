# README

## How to run project with docker

Build images, bundle install, yarn install
```
docker-compose build
docker-compose run -u root backend bundle
docker-compose run frontend yarn
```

## Run bash in containers

* On db server
```
docker exec -it rails-nuxt-dashboard_db_1 bash
```
* On backend server (rails)
```
docker exec -it rails-nuxt-dashboard_backend_1 bash
```
* On frontend server (nuxtjs)
```
docker exec -it rails-nuxt-dashboard_frontend_1 bash
```
