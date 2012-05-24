nginx-debian-squeeze
====================

My custom changes to the nginx Debian source package

Instructions
============

Follow instructions on http://nginx.org/en/download.html to add nginx repositories to APT.

Do not install nginx, but fetch the source package with:

    apt-get source nginx

You will also need build tools and build dependencies for nginx:

    apt-get install build-essential
    apt-get build-dep nginx

You will get an nginx-1.2.0 folder, the content of this folder is what is stored in this repository.

The changes made:

- added modules directory with modules ngx_cache_purge-1.5 & ngx_http_redis-0.3.5
- changed debian/rules file to add these two modules and fine tunes nginx config for my needs
