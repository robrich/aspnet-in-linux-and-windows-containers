FROM mcr.microsoft.com/dotnet/core/sdk:3.1

VOLUME ["/app", "/app/bin", "/app/obj"]

WORKDIR /app

ENV ASPNETCORE_URLS http://+:5000
ENV ASPNETCORE_ENVIRONMENT Development
EXPOSE 5000
# builds and runs, sticking built content into volumes
CMD dotnet build && dotnet watch run
