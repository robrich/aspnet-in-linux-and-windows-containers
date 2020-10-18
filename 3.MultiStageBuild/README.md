Multi-stage Build
=================

In this step we introduce multi-stage builds and highlight how it makes the resulting containers so much smaller.

## Run it

```sh
docker-compose up --build
```

Then browse to http://localhost:80/

When you're done, hit cntrl+c and run `docker-compose down` to stop the container.

Run `docker image list` to see the size difference between this step and step1.
