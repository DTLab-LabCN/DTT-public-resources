# DTT-public-resources
Public resources for DTT development


## POSTMAN

Download the postman desktop client
https://www.postman.com/downloads/

Create a new workspace

Import the following environments:

- [local](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/Local.postman_environment.json)

Import the following collections:

- [workspaces](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/01-Workspaces.postman_collection.json)
- [backchannels](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/02-Backchannels.postman_collection.json)
- [test-harness](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/03-Test-harness.postman_collection.json)


## DOCKER

For local development, you need redis/postgres instances.

Run the provided docker-compose file to get these up and running:

```
docker-compose up -d
```

You will have postgres (localhost:5432), redis (localhost:6379) and pgadmin (localhost:15433) instances available.
Use these values in your local .env configurations


## Startup script

Quickly get the frontend backend up with our utility script

You must have tmux installed and be connected to the vpn.

```
./start.sh
```

If you have an application blocking these ports, use this command with caution, it will kill whatever process is running on the port.
Useful if you loose a tmux shell.
```
fuser -k 5000/tcp
fuser -k 8000/tcp
```