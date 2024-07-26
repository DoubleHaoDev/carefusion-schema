# carepulse-schema
Liquibase repo for carepulse app

./gradlew status to view unexecuted changeSets ./gradlew update to update DB with existing changeSets ./gradlew rollbackCount -PliquibaseCommandandValue=1 to rollback changes



sudo docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=bafoZhjW_3k-" \
-p 1433:1433 --name carepulse_development --hostname carepulse_development \
-d \
mcr.microsoft.com/mssql/server:2022-latest
docker run -e 'ACCEPT_EULA=1' -e 'MSSQL_SA_PASSWORD=bafoZhjW_3k-' -p 1433:1433 --name carepulse_development -d mcr.microsoft.com/azure-sql-edge
