# MondoDb-Docker-Compose

1.Create this file in VSCode in a separate blank project

docker-compose.yml

```yaml
version: "3.3"

services:
 mongodb:
   image: mongo:latest
   container_name: mongodb
   environment:
    MONGO_INITDB_ROOT_USERNAME: 
    MONGO_INITDB_ROOT_PASSWORD: 
   ports:
    - 27017:27017
   volumes:
    - .dbmongodb:/var/lib/lib/mongodb
```

2.To run the MondDb container run the command, open this project in VSCode and run the command: 

docker-compose up

IMPORTANT NOTE: Do not forget to set the USERNAME and PASSWORD. We recomend you to leave boths fields in blank.

3.Run MondoDb Compass and connect to the MongoDb docker container
Set the connection string: mongodb://localhost:27017

NOTE: in case we set a USERNAME and PASSWORD for the MondDb container
use this connection string: mongodb://admin:admin@localhost:27017

4.Create a new database and a new collection. For example:
Database name: nodejs
Collection name: home

