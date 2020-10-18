FROM mcr.microsoft.com/dotnet/core/aspnet:3.1

WORKDIR /app
COPY dist .

ENV ASPNETCORE_ENVIRONMENT Production
ENV ASPNETCORE_URLS http://+:80
EXPOSE 80

CMD ["dotnet", "Site.dll"]
