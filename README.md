# CareFusion-schema
Liquibase repo for CareFusion app
## Docker Operations
### Docker Pull Image
This project uses postgresql 16.3. <br/>
To download postgresql official image, run the following command in the terminal:<br />
`docker pull postgres:16.3`
Once the image is pulled, run <br/>
`docker image list` to check if image exists.
### Docker Container Operations
For the very first time, run the following command for a quick start:<br />
`docker run -d --name carefusion_development -e POSTGRES_PASSWORD=carefusion -p 5432:5432 postgres`
Run the following command to stop carefusion_development container:<br/>
`docker stop carefusion_development`
Run the foloowing command to restart carefusion_development container:<br/>
`docker start carefusion_development`
### Register PostgreSQL Server
Once the container is running, use pgAdmin to connect to the database.
1. Right Click on `Servers` -> `Register` -> `Server...`
2. In register dialog, give the server a name. e.g dockerDB
3. Switch to connection tab, input `localhost` host name section
4. Input `carefusion` in the password text field and Save.
5. Right click on `dockerDB` -> `Create` -> `Database...`
6. Input `carefusion_development` for Database name and save.

## Liquibase
### Run Liquibase Changesets
Once the postgresql server is all set, run <br/> 
`./gradlew status` to view unexecuted changeSets<br/>
`./gradlew update` to update DB with existing changeSets<br/>
`./gradlew rollbackCount -PliquibaseCommandValue=1` to rollback changes

## Useful Docker Commands
### Docker List of Containers
`docker ps -a`
