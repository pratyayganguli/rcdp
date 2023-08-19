
## Redis Certified Developer Program ##

### Redis University ###

Handy [docker](pages/docker-commands) commands 

#### Installation of Redis ####

Running a redis container:

```bash
docker run --name <container_name> -d redis
```

Launch the redis container:

```bash
docker exec -it <container_name> redis-cli
```

Accessing the **redis.conf** file to modify the properties of your redis server.

1. Create a Dockerfile and paste the following contents
    ```Dockerfile
    FROM redis:latest
    COPY redis.conf /usr/local/etc/redis/redis.conf
    CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]
    ```

    ```bash
    docker exec -it <container_name> cat /usr/local/etc/redis/redis.conf
    ```
    
Understanding strings:
    ```
        SET key "value"
        GET key
    ```

