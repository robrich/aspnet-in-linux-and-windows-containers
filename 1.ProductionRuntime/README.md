Production Runtime
==================

In this example, we build on our regular file system, and only copy built assets into the container.

## Run it

```sh
dotnet build --configuration Release
dotnet publish -c Release -o dist
docker build -t step1 .
docker run -p 80:80 step1
```

Then browse to http://localhost:80/

When you're done, use these commands to stop the container:

```sh
docker container list
# locate the container name or id
docker container stop container_name_here
docker container rm container_name_here
```

With the container stopped and removed, browse to http://localhost:80/ and you'll get a web error.  The site no longer exists.
