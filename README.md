# digiblink/alpine-nginx-php74-fpm Docker Container

Maintained by [digiBlink](https://digiblink.eu) - [docker hub link](https://hub.docker.com/r/digiblink/alpine-nginx-php74-fpm/)

Container with:

* Alpine Linux 3.12 
* nginx 1.18.0-r1
* PHP-FPM 7.4.12 (all necessary extensions to be ready for Wordpress deployment)
* [WP-CLI](https://wp-cli.org) 2.4.0
* git, bash

## Usage

To get it running just enter:

`docker run -d --name your_container -v /sites/yourdomain.com:/DATA -p 80:80 -t digiblink/alpine-nginx-php74-fpm`

After that you can use BusyBox bash, to log into container and use [WP-CLI](http://wp-cli.org), to install [WordPress](https://wordpress.org):

`docker exec -ti your_container bash`

After logging in issue following commands:

```
su www-data
cd /DATA
wp-cli
```
