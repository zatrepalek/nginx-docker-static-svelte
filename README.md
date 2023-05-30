# nginx-docker-static-svelte

Docker image with basic Nginx server for [Svelte static adapter](https://kit.svelte.dev/docs/adapter-static). With this image there is no need for `trailingSlash = 'always'` settings.

## Usage

You can serve your static build e.g. using docker-compose like this:

```
version: '3'

services:
  foo:
    container_name: foo
    image: zanne/nginx-docker-static-svelte:latest
    restart: unless-stopped
    ports:
      - 80:80
    volumes:
      - /dir/with/contents:/usr/share/nginx/html
```
