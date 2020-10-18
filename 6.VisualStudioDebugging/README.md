Visual Studio Debugging
=======================

This project introduces container debugging inside Visual Studio.  See also https://docs.microsoft.com/en-us/visualstudio/containers/tutorial-multicontainer

## Run it

1. Open this project in Visual Studio.

2. Inside the WebApplication project, put a breakpoint inside HomeController inside the Privacy method.

3. Inside the WebAPI project, put a breakpoint inside the WeatherForecast controller.

4. Switch the debugger to docker-compose.

5. Start debugging.

6. Your default browser opens automatically.

7. Click Privacy to launch the target method.

   Note how we hit the breakpoint in the WebApplication project.

8. Push go.

   Now we hit the breakpoint in the WebAPI project

9. Push go.

   Now we see the rendered results.

Note that IIS Express isn't running, and running `docker container list` shows the code running inside Docker.

When you're done, stop debugging, and close Visual Studio.
