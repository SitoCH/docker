README
======

## About ##

This image deploys a PHP FPM container configured to handle OwnCloud.
This is especially useful when you want two different instances to handle the "normal" traffic and OwnCloud.

## Usage ##

To run the image sito/php-fpm-oc, execute the following command:

```
docker run -d  -p 9000:9000 --name=php-fpm --restart=always -v /var/www:/var/www sito/php-fpm-oc
```

## Notes ##

You can override the default settings with two ENV variables.
To change the default memory limit:

```
-e MEMORY_LIMIT=512M
```

And to change the default timezone:

```
-e TIMEZONE=Europe/Paris
```

Please be aware that this image uses "/var/www" as website path.