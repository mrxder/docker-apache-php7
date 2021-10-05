## Apache2 with php7 on Ubuntu 16.04 LTS for Development

This docker image is a fork from nimmis/apache-php7.

This is a docker images with  Ubuntu 16.04 LTS with apache2 and php7/composer

To access site contents from utside the container you should map /var/www

Includes composer for easy download of php libraries

### Examples

Start container without mapping local files. This is useful if you want to access the container directly.
```
docker run --rm -d -p 8080:80 mrxder/apache-php7-dev
```

Start the webserver to host local files. This command maps the content of the actual directory to the webserver root folder.
```
docker run -rm -d -p 8080:80 -v "$PWD:/var/www/html" mrxder/apache-php7-dev
```

The docker container is started with the -d flag so it will run inte the background. To run commands or edit settings inside
the container run `docker exec -ti <container id> /bin/bash'
 
