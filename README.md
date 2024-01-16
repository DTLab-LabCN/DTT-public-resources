# DTT-public-resources
Public resources for DTT development


## POSTMAN

Download the postman desktop client
https://www.postman.com/downloads/

Create a new workspace

Import the following environments:

- [local](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/Local.postman_environment.json)

Import the following collections

- [workspaces](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/01-Workspaces.postman_collection.json)
- [backchannels](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/02-Backchannels.postman_collection.json)
- [test-harness](https://raw.githubusercontent.com/IDLab-org/DTT-public-resources/main/postman/03-Test-harness.postman_collection.json)


## DOCKER

For local development, you need redis/postgres instances.

Run the provided docker-compose file to get these up and running:

```
docker-compose up -d
```

You will have postgres, redis and pgadmin instance available


## Startup script

Quickly get the frontend backend up with our utility script

You must have tmux installed and be connected to the vpn.

```
./start.sh
```