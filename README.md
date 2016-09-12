## docker-php7
Dockerfile for Apache PHP-7 and Ubuntu 14.04


Basic packages

- Apache
- PHP 7.0.10
    - Extensions
        - Geoip 
        - Aerospike 
        - Memcached 
        - Imagick
        - Xdebug

### Usage

* To build the image

```
docker build -t rmondragon/php7 .
```

* The following will run `rmondragon/php7` default setup though port 8080. To check phpinfo, browse http://localhost:8080/phpinfo.php

```
docker run -d -p 8080:80 --name <CONTAINER_NAME> rmondragon/php7
```

* To mount your local php project, and it will start in <PATH>/htdocs

```
docker run -d -p 8080:80 -v <PATH>:/var/www --name php7 rmondragon/php7
```


# Supported Docker versions

This image is officially supported on Docker version 1.12

# User Feedback

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/rmondragon/docker-php5/issues).


## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.
