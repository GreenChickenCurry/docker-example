FROM mcr.microsoft.com/dotnet/sdk:7.0 as build
 
WORKDIR /src
COPY ./app/app.csproj ./
RUN dotnet restore
 
COPY ./app ./
RUN dotnet build -o /project
RUN dotnet publish -o /publish
 
FROM mcr.microsoft.com/dotnet/aspnet:7.0 as base
COPY --from=build  /publish /project
WORKDIR /project

EXPOSE 5000
CMD ["./app"]
