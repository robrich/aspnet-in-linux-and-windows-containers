FROM mcr.microsoft.com/dotnet/aspnet:5.0

WORKDIR /app

COPY dist .

ENV ASPNETCORE_ENVIRONMENT Production
ENV ASPNETCORE_URLS http://+:80
EXPOSE 80

CMD ["dotnet", "Site.dll"]
