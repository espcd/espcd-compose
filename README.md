# espcd-compose

Docker-compose production config.

## Usage

Open the `.env` file and adjust the environment variables.

### Update

```
docker-compose pull && docker-compose build
```

Pulls container images and build containers.

### Start

```
docker-compose up -d
```

Starts all containers.

SSL certificates are automatically created for the backend and frontend host at the first startup. These certificates are renewed periodically. After a few seconds the fontend is available at the host defined in the `FRONTEND_HOST` environment variable, e.g.: https://espcd.duckdns.org/.

### Stop

```
docker-compose down
```

Stops all containers.
