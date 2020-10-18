FROM mcr.microsoft.com/dotnet/core/sdk:3.1

WORKDIR /src

COPY . .

RUN dotnet restore

RUN dotnet build -c Release

RUN dotnet test

RUN dotnet publish -c Release -o /app Site/Site.csproj


WORKDIR /app

ENV ASPNETCORE_ENVIRONMENT Production
ENV ASPNETCORE_URLS http://+:80
EXPOSE 80

CMD ["dotnet", "Site.dll"]
