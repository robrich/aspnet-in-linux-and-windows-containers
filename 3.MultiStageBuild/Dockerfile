# Build server:
FROM mcr.microsoft.com/dotnet/sdk:5.0-alpine as build

WORKDIR /src

COPY Site.sln .
COPY Site/Site.csproj Site/
COPY Site.Tests/Site.Tests.csproj Site.Tests/
RUN dotnet restore

COPY . .
RUN dotnet build -c Release
RUN dotnet test
RUN dotnet publish -c Release -o /dist Site/Site.csproj

# Production server
FROM mcr.microsoft.com/dotnet/aspnet:5.0-alpine

ENV ASPNETCORE_ENVIRONMENT Production
ENV ASPNETCORE_URLS http://+:80
EXPOSE 80

WORKDIR /app

COPY --from=build /dist .

CMD ["dotnet", "Site.dll"]
