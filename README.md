# docker-nginx-debian
Docker: Nginx With All Official Modules And Some Third Party Modules (Based On Debian)

# Third Party Modules
```
Jemalloc (Share Library)
Redis (Software)
OpenSSL (Just Build Into The Nginx)
Nginx Module:Cache-Purge
Nginx Module:Brotli
Nginx Module:PageSpeed
Nginx Module:Redis
Nginx Module:Devel-Kit
Nginx Module:Set-Misc
Nginx Module:Echo
Nginx Module:Redis2
Nginx Module:Srcache
```

# Usage
```
$ docker pull xaster/docker-nginx-debian

$ docker run -d \
    --name docker-nginx-debian \
    -v /NGINX_WEB_DIR:/usr/share/nginx/html \
    -v /NGINX_CONFIG_DIR:/etc/nginx \
    -v /NGINX_CERTS_DIR:/etc/certs \
    -v /NGINX_LOG_DIR:/var/log/nginx \
    -v /NGINX_CACHE_DIR:/var/cache/nginx \
    -v /NGINX_RUN_DIR:/var/run/nginx \
    -v /REDIS_CONFIG_DIR:/etc/redis \
    -v /REDIS_LOG_DIR:/var/log/redis \
    -v /REDIS_DATA_DIR:/var/lib/redis \
    -v /REDIS_RUN_DIR:DATA/var/run/redis \
    -p 80:80 \
    -p 443:443 \
    -p 6379:6379 \
    -e TIMEZONE=YOUR_TIME_ZONE \
    xaster/docker-nginx-debian
```

# Note
```
80=http listen port
443=https listen port
6379=redis listen port
```
