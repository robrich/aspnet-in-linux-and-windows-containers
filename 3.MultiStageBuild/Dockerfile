FROM mcr.microsoft.com/dotnet/core/sdk:3.1 as build

WORKDIR /src

COPY Site.sln .
COPY Site/Site.csproj Site/
COPY Site.Tests/Site.Tests.csproj Site.Tests/
RUN dotnet restore

COPY . .

RUN dotnet build -c Release

RUN dotnet test

RUN dotnet publish -c Release -o /dist Site/Site.csproj


FROM mcr.microsoft.com/dotnet/core/aspnet:3.1

WORKDIR /app
COPY --from=build /dist .

ENV ASPNETCORE_ENVIRONMENT Production
ENV ASPNETCORE_URLS http://+:80
EXPOSE 80

CMD ["dotnet", "Site.dll"]
