#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

#Set the base image to the .NET 6 SDK
FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /app

# Copy the project files and restore dependencies
COPY HotReload.Sample.API/HotReload.Sample.API.csproj .
RUN dotnet restore

# Copy the remaining project files
COPY . .

# Start the application in watch mode
CMD ["dotnet", "watch", "run", "--project" , "HotReload.Sample.API/HotReload.Sample.API.csproj",  "--urls", "https://*:443;http://*:80"]