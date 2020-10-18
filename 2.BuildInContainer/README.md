Build in Container
==================

In this step, we build inside the container, add unit tests, and introduce docker-compose.

## Run it

```sh
docker-compose build
docker-compose up
```

Then browse to http://localhost:80/

When you're done, hit cntrl+c and run `docker-compose down` to stop the container.

Try making a failing test or modifying the code to make the compile fail, then re-run the commands.
