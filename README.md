# Docker Swarm

This cluster consists of following services.

*cake-test_myapp-mysql (Mysql V8.0)*
*cake-test_myapp-php-fpm (PHP V8.0)*
*cake-test_myapp-nginx (webserver to handle requests)*
*cake-test_myapp-nginx-reverse-proxy (Load balancer)*
*cake-test_myapp-nginx-health-check (Health check)*

## Deployment
Login to manager node and clone the repo and then run:

```
docker stack deploy --compose-file docker-compose.yml cake-test
```
