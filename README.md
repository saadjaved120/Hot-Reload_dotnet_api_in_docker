# Hot reload dotnet app in docker
Find details here: 

### Running application 
Create trusted certificate on local machine by running following command individually on terminal
```
dotnet dev-certs https --clean

dotnet dev-certs https -ep "$env:USERPROFILE\.aspnet\https\aspnetapp.pfx" -p 123 

dotnet dev-certs https --trust
```
To run the application, open CMD/Powershell in the solution directory of porject and run follwing command:
```
docker compose up
```
application will be running on URL:
```
https://localhost:5001/swagger
```
