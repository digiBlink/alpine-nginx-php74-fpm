# digiblink/alpine-nginx-php74-fpm Docker Container

Maintained by [digiBlink](https://digiblink.eu) - [docker hub link](https://hub.docker.com/r/digiblink/alpine-nginx-php74-fpm/)

Container with:

* Alpine Linux 3.20 (with latest security updates)
* nginx 1.26.2-r0
* PHP-FPM 7.4.33 (all necessary extensions to be ready for Wordpress deployment)
* WP-CLI 2.11.0
* git, bash

## Usage

To get it running just enter:

`docker run -d --name your_container -v /sites/yourdomain.com:/DATA -p 80:80 -t digiblink/alpine-nginx-php74-fpm`

After that you can use BusyBox bash, to log into container and use [WP-CLI](http://wp-cli.org), to install [WordPress](https://wordpress.org):

`docker exec -ti your_container bash`

After logging in to manage WordPress issue following commands:

```
su www-data
cd /DATA/htdocs/current
wp-cli
```
