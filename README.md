# Flights-Alert-Management

# README

## Prerequisites

1. Install Docker on your system.
2. Pull the SQL Server Docker image:
   ```bash
   docker pull mcr.microsoft.com/mssql/server:2019-latest
   ```
3. Run the SQL Server Docker container:
   ```bash
   docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=aaa" -p 1433:1433 --name sqlserver -d mcr.microsoft.com/mssql/server:2019-latest
   ```

## Running the Application

1. Ensure the SQL Server container is running. You can check with:
   ```bash
   docker ps
   ```
2. Use the following connection details for the SQL Server:
   - **Server name**: `localhost`
   - **Authentication**: SQL Server Authentication
   - **Login**: `sa`
   - **Password**: `aaa`

3. Run your .NET Core application. Make sure it connects to the SQL Server instance using the above credentials.

## Additional Information

To stop the SQL Server container, run:
```bash
docker stop sqlserver
```

To remove the container, run:
```bash
docker rm sqlserver
```

