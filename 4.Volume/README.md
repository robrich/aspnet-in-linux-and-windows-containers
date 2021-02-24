Build in a Volume
=================

In this example we use a volume to quickly iterate on the website while it's running in the container.

## Run it

```sh
docker build -t 4volume -f Dockerfile.dev .
docker run -p 5000:5000 -v "$pwd:/app" -v /app/bin -v /app/obj 4volume
```

While the site is running, change some code, then watch the console to see the site rebuild.

When you're done, use these commands to stop the container:

```sh
docker container list
# locate the container name or id
docker container stop container_name_here
docker container rm container_name_here
```
