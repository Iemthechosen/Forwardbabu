# not yet ready

It is assumed that you are familiar with basic `docker` commands.

Make sure you have understood how `telewater` is run by passing certain variables via [command-line options](https://github.com/aahnik/tgcf/wiki/CLI-usage) or by setting them as [environment variables](https://github.com/aahnik/tgcf/wiki/Environment-Variables). 

## Install

Docker should be properly installed and running in your system.

```shell
$ docker pull aahnik/tgcf
```

## Run

Write all your [environment variables](https://github.com/aahnik/telewater/wiki/Environment-Variables#create-a-env-file) in a file called `.env` and then use the `docker run` command to start the bot.

```shell
$ docker run -d --env-file .env aahnik/tgcf
```

Note:
- the `-d` flag tells the docker command to run the container in detached mode.
- the `--env-file` option passes the file `.env` for its variables to be used inside the container.


## Check

To see if your container is running,

```shell
$ docker ps
CONTAINER ID   IMAGE               COMMAND       CREATED          STATUS          PORTS     NAMES
ae4d7d6651ca   aahnik/tgcf    "poetry run tgcf"   3 minutes ago    Up 3 minutes              zen_gates

```

The container id and name will be different in your machine.

To see the logs produced by the container,

```shell
$ docker logs zen_gates
```

Replace `zen_gates` with the name of the container in your machine.



