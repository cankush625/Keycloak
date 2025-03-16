# Keycloak

## Command to build the image on Mac M4
```
$ docker build . --no-cache --tag keycloak:latest --platform linux/amd64
```

## Command to start the Keycloak service
```
$ docker run --name mykeycloak --network=bridge -p 4000:8443 -p 4001:8080 -p 9001:9000 \
    -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=change_me -e KC_HTTP_ENABLED=true \
    keycloak:latest start-dev
```
