# Docker

## Local

## Production, Staging and Dev

## Debugging

| Command | Description | Arguments |
|---|---|---|
| `docker logs {service_name}` | View the logs of a specific service. | `-f`: follow in real time, `--tail N`: return last N lines |
| `docker ps` | List running container services. | |
| `docker stats` | View the stats of all the runing container services. | |

### Common issues

__502__

- Check all the proxy services are running.
- Check all of your container services are running.
- Check `VIRTUAL_HOST` is set, and used in the service correctly

__503__

- Check your container services are running.
- Check your language service (`PHP`, `node`, etc) does not have a `VIRTUAL_HOST` set.

If all else fails, run `docker logs your_service_name`.
