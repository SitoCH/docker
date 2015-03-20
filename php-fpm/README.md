README
======

## About ##

This image deploys a PHP FPM container configured to handle OwnCloud.
This is especially useful when you want two different instances to handle the "normal" traffic and OwnCloud.

## Usage ##

To run the image sito/php-fpm-oc, execute the following command:

```
docker run -d  -e FPM_PORT=9001 --name=php-fpm-oc --net=host --restart=always -v /var/www:/var/www sito/php-fpm-oc
```

## Notes ##

You can override the default settings with two ENV variables.
Change the default port used to listen for new connections:

```
-e FPM_PORT=9001
```

And to change the default timezone:

```
-e TIMEZONE=Europe/Paris
```

Please be aware that this image shares the host networking and uses "/var/www" as website path.