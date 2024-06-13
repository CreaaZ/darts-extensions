# Containerized Autodarts Extensions

The following repository contains a containerized setup for Autodarts extensions with Nginx Proxy Support using Docker Compose.
At the moment, the following extensions are supported:

- [darts-caller](https://github.com/lbormann/darts-caller)
- [darts-wled](https://github.com/lbormann/darts-wled)

## Running the Compose File(s)

The compose files are modularized, so that individual setups can be easily created.
The basic setup with _darts-caller_ is defined in `compose.yaml`.
To run this, simply execute:

```docker compose up```

If you want to add the Nginx Proxy Manager to your stack and expose the endpoint(s) through Nginx, you can combine multiple compose files:

```docker compose -f compose.yaml -f compose.proxy.yaml up```

Please note that the files must always be specified using `-f` when starting/stopping the containers through `docker compose up|down`

