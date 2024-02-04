## Description
"next_laravel_dev_with_docker" is a repository that configures a local development environment to seamlessly integrate NEXT JS and Laravel. By setting up this environment, accessing http://localhost/ opens a NEXT JS page, while http://localhost/server/ leads to a Laravel page. This setup facilitates easy development and testing for projects combining the power of NEXT JS for the frontend and Laravel for the backend, all within a Dockerized environment for consistency across different machines.

## How to work?🤔
```
docker volume create --name=front_node_modules
docker volume create --name=composer_files
docker network create omoide_networks
docker-compose -f docker-compose-local.yml build
docker-compose -f docker-compose-local.yml run user-front npm install
docker-compose -f docker-compose-local.yml run backend-laravel composer install
docker-compose -f docker-compose-local.yml up
```