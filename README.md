# coldrye-debian-nginx

[![coldrye/debian-nginx](http://dockeri.co/image/coldrye/debian-nginx)](https://hub.docker.com/r/coldrye/debian-nginx/)


## Description

This packages Debian in various releases based on coldrye/debian-tini for containerized services based on nginx.

Using this image, one can easily create reverse proxies a/o application servers.


## Image Releases

Images are released for the following debian releases.

- jessie
- testing (stretch)

See https://hub.docker.com/r/coldrye/debian-nginx/tags/ for a complete list.


## Additional Packages

### Networking

- nginx-full


## Start Command

The start command is set to ["/usr/sbin/nginx"] and ``daemon off;`` is added to ``/etc/nginx/nginx.conf`` so
that it won't detach.


## Configuring NGINX

Since this is a standard Debian NGINX installation, one can edit a/o add configuration files to /etc/nginx.
Site configuration should be added to ``/etc/nginx/sites-enabled`` rather than ``/etc/nginx/sites/available``
and creating symlinks in ``/etc/nginx/sites-enabled``.


## Reload NGINX

Using ``docker exec <CONTAINER> "/usr/sbin/nginx -s reload;exit"`` one can reload the configuration
without having to restart the container.

